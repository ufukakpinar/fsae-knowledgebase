When multiple lithium-ion battery cells are joined in prallel to increase current and power output capabiltiy a critical safety problem arises. With the high energy density and very low internal resistance of these high performance cells a significant safety hazard is presented in the case of cell failure. If just one cell out of many cells in a parallel stack shorts out this could result in the thermal runaway of the entire stack as all of the cells would be practically get shorted out and try release all of their energy at once. This could result in a cascading effect that can cause the whole battery pack to catch fire. To safeguard against this possibility we must implement cell level fuses that will trip in case of cell failure and contain the damage to the failed cell.

We must start the design considerations of the fuse with some operational parameters:

## Fault Current Under Short Circuit Condition

When a cell is shorted either by external or internal factors the maximum theorethical fault current can be calculated by dividing the maximum cell voltage by the internal resistance of the cell. The cell fuse must have an interrupt rating that is equal to this fault current minimum to ensure the failure can be safely contained. It is important to test the cell fuse with this theorethical maximum fault current to certify it for service.

## Current Carrying Requirements

Since these cell level fuses are only meant to be safeguards against catasthrophic events and their tripping would severely affect the performance of the pack special care must be taken to ensure that they will not trip under normal operating conditions. Since most cell level fuses are used in conjunction with a master fuse on the main current path it is important to coordinate the performance of these fuses. The main pack should trip before any single cell fuse unless a short circuit condition of a cell is present. 

While an easy way to ensure this is to rate the cell fuse above the operating capabiltiies of the cell and the master fuse, it is important to consult manufacturer recommendations and ensure that the cell level fuse trips before the maximum pulse current specification of the cell is exceeded.

As an example the Samsung INR18650-25R used above for fault current analysis has a recommended maximum pulse current of 100A for 1 second. This number can be used as a constraint to ensure the cell level fuse acts fast enough to disconnect the cell from the circuit before the cell gets damaged.

In summary:
  1. The cell level fuse must not trip at the rated current or any pulses not exceeding the cell specification.
  2. The cell level fuse should be designed to trip after the tripping point of the master pack fuse.
  3. The cell level fuse should not allow the cell to exceed its maximum pulse discharge specification.
