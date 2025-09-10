# TODO: Enforce Access Control for Inventories and Items

## Current Status
- [x] Analyze existing access control in InventoriesController.cs
- [x] Analyze ItemsController.cs for missing access controls
- [x] Create implementation plan
- [x] Get user approval for plan

## Pending Tasks
- [x] Add access control checks to ItemsController.cs Create (POST) action
- [x] Add access control checks to ItemsController.cs Edit (POST) action
- [x] Add access control checks to ItemsController.cs Delete (POST) action
- [x] Add access control checks to ItemsController.cs Create (GET) action
- [x] Add access control checks to ItemsController.cs Edit (GET) action
- [ ] Check for missing access controls in InventoriesController.cs
- [ ] Test the access control implementation
- [ ] Update documentation if needed

## Implementation Details
- Access control logic: User must be inventory owner OR admin OR have granted access OR inventory is public
- Use similar logic as in InventoriesController.HasAccessToInventory method
- Return Forbid() for unauthorized access attempts
