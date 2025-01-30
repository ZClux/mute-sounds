local store = {}

for i, object in pairs(workspace:GetDescendants()) do

    if object.ClassName == "Sound" then

        table.insert(store, #store + 1, {['Object'] = object, ['Vol'] = object.Volume})

        object.Volume = 0 -- change Volume to 0 after storing it in the store table

    end

end
