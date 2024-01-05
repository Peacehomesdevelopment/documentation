============
LIFO removal
============

The *last in, first out* (LIFO) removal strategy picks the **newest** products on-hand based on the
date they entered a warehouse's stock.

Every time an order for products with the :abbr:`LIFO (Last In, First Out)` method is placed, a
transfer is created for the lot/serial number that has most recently entered the stock (the **last**
lot/serial number that entered the warehouse's inventory).

.. warning::
   In many countries, the :abbr:`LIFO (Last In, First Out)` removal strategy in banned, since it can
   potentially result in old, expired, or obsolete products being delivered to customers.

Consider the following product, `Cinder Block`, which is tracked :guilabel:`By Lots` in the
:guilabel:`Inventory` tab of the product form, and its product category's :guilabel:`Force Removal
Strategy` is set to :guilabel:`Last In, First Out (LIFO)`.

.. seealso::
   - :ref:`Set up force removal strategy <inventory/routes/strategies/set>`
   - :ref:`Enable lots tracking <inventory/removal/lots-setup>`
   - :ref:`Check arrival date <inventory/removal/arrival_date>`

The following table represents the cinder blocks in stock and their various lot number details.

.. list-table::
   :header-rows: 1
   :stub-columns: 1

   * -
     - LOT1
     - LOT2
     - LOT3
   * - On-hand stock
     - 10
     - 10
     - 10
   * - :ref:`Created on <inventory/removal/arrival_date>`
     - June 1
     - June 3
     - June 6

To see the removal strategy in action, create a :ref:`delivery order <inventory/delivery/one-step>`
for seven cinder blocks, either by going to the :menuselection:`Sales app` and create a new
quotation, or from the delivery orders dashboard in :menuselection:`Inventory --> Operations -->
Deliveries`. :guilabel:`Confirm` the sales order or click :guilabel:`Mark as Todo` on the draft
delivery order.

Doing so creates the delivery order, and the newest lot numbers are reserved according to the
:abbr:`LIFO (Last In, First Out)` removal strategy.

To view the detailed pickings, click the :guilabel:`⦙≣ (bulleted list)` icon on the far right of the
cinder block's product line in the :guilabel:`Operations` tab of the delivery order. Doing so opens
the :guilabel:`Open: Stock move` pop-up window.

In the :guilabel:`Open: Stock move` window, the :guilabel:`Pick from` field details where the
quantities to fulfill the :guilabel:`Demand` are picked from. Since the order demanded seven cinder
blocks, the newest cinder blocks from `LOT3` are selected using the :abbr:`LIFO (Last In, First
Out)` removal strategy.

.. image:: lifo/cinder-block-picking.png
   :align: center
   :alt: The detailed operations shows which lots are being selected for the picking.
