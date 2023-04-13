# Calculate number of prarameters in model
```python
# Total parameters
sum(p.numel() for p in model.parameters())
# Trainable & Untrainable params
sum(p.numel() for p in model.parameters() if p.requires_grad) # Trainable
sum(p.numel() for p in model.parameters() if not p.requires_grad) # Untrainable
```
