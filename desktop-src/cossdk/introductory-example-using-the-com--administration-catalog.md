---
description: Exemple d’introduction utilisant le catalogue d’administration COM+
ms.assetid: e9ce25aa-4fb1-4357-9f4e-5bf649e29447
title: Exemple d’introduction utilisant le catalogue d’administration COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db24f3985538b7189534c9fef3ef279ed240e3a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311017"
---
# <a name="introductory-example-using-the-com-administration-catalog"></a>Exemple d’introduction utilisant le catalogue d’administration COM+

Par programmation, en utilisant le catalogue d’administration COM+, vous effectuez généralement les étapes générales suivantes (non fournies dans un ordre strict ici) :

-   Ouvrez une session avec le catalogue COM+ sur l’ordinateur local. Si vous le souhaitez, connectez-vous au catalogue COM+ sur un ordinateur distant.
-   Effectuer des actions telles que le démarrage ou l’arrêt des services, qui ne concernent pas une application COM+ particulière.
-   Effectuer des actions telles que l’installation ou l’exportation d’applications COM+, ou l’installation de composants dans des applications, des actions relatives à la lecture ou à l’écriture dans des fichiers.
-   Ajoutez de nouveaux éléments aux regroupements, tels que la création d’une application COM+ en ajoutant un nouvel élément au regroupement « applications ».
-   Définir ou obtenir des propriétés sur un élément d’une collection.
-   Enregistrez ou ignorez les modifications en attente dans le catalogue.
-   Gérer les erreurs qui peuvent se produire.

pour voir à quoi ressemblent ces étapes lorsque vous utilisez les objets comadmin, un exemple de Visual Basic Microsoft est fourni ci-dessous. Il illustre brièvement certaines des étapes classiques décrites ci-dessus, telles que la localisation des collections, l’énumération d’une collection pour récupérer un élément et la définition des propriétés de cet élément.

Dans l’exemple ci-dessous, vous allez effectuer les actions suivantes :

1.  Créez une nouvelle application COM+, « MyHomeZoo ».
2.  Installez des composants, des chats et des chiens dans l’application. Les deux composants sont contenus dans une DLL unique qui doit déjà exister : MyZoo.dll.
3.  Configurez la sécurité basée sur les rôles pour l’application en définissant deux rôles : ZooKeeper et AllergicToCats.
4.  Attribuez l’accès au rôle ZooKeeper à l’application entière.
5.  Attribuez l’accès au rôle AllergicToCats uniquement au composant chien.
6.  Activez les propriétés de sécurité pour appliquer la vérification des rôles à l’application.
7.  Exportez l’application MyHomeZoo dans un fichier pour qu’elle puisse être installée sur d’autres ordinateurs.

pour utiliser cet exemple à partir de Visual Basic, ajoutez une référence à la bibliothèque de types d’administration COM+.


```VB
Function SetupMyZoo() As Boolean  ' Return False if any errors occur.

    '  Initialize error handling for this function.
    SetupMyZoo = False 
    On Error GoTo My_Error_Handler

    '  Open a session with the catalog.
    '  Instantiate a COMAdminCatalog object. 
    Dim objCatalog As COMAdminCatalog
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")

    '  Create a new COM+ application.
    '  First get the "Applications" collection from the catalog.
    Dim objApplicationsColl As COMAdminCatalogCollection
    Set objApplicationsColl = objCatalog.GetCollection("Applications")

    '  Add a new item to this collection. 
    Dim objZooApp As COMAdminCatalogObject
    Set objZooApp = objApplicationsColl.Add

    '  The "Applications" collection determines the available properties.
    '  Set the "Name" property of the new application item. 
    objZooApp.Value("Name") = "MyHomeZoo"

    '  Set the "Description" property of the new application item. 
    objZooApp.Value("Description") = "My pets at home"

    '  Save changes made to the "Applications" collection. 
    objApplicationsColl.SaveChanges

    '  Install components into the application.
    '  Use the InstallComponent method on COMAdminCatalog. 
    '  In this case, the last two parameters are passed as empty strings.
    objCatalog.InstallComponent "MyHomeZoo","MyZoo.DLL","","" 

    '  Define the roles ZooKeeper and AllergicToCats 
    '  by adding them to the "Roles" collection related to MyHomeZoo. 
    '  First get the "Roles" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Roles", 
    '  and the Key property value of objZooApp.   
    '  The Key property uniquely identifies the object, serving
    '  here to distinguish the "Roles" collection related 
    '  to MyHomeZoo from that of any other application. 
    Dim objRolesColl As COMAdminCatalogCollection
    Set objRolesColl = objApplicationsColl.GetCollection("Roles", objZooApp.Key)

    '  Add new items to this "Roles" collection. 
    Dim objZooKeeperRole As COMAdminCatalogObject
    Dim objAllergicToCatsRole As COMAdminCatalogObject
    Set objZooKeeperRole = objRolesColl.Add
    Set objAllergicToCatsRole = objRolesColl.Add

    '  Set the "Name" for the new items.
    objZooKeeperRole.Value("Name") = "ZooKeeper" 
    objAllergicToCatsRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to any items in this "Roles" collection. 
    objRolesColl.SaveChanges

    '  Assign the AllergicToCats role to the Dog component to 
    '  restrict its scope of access. (The ZooKeeper role, if assigned
    '  only at the application level, can access the whole application.)
    '  First get the "Components" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Components", and
    '  the Key property value of objZooApp. 
    Dim objZooComponentsColl As COMAdminCatalogCollection
    Set objZooComponentsColl = objApplicationsColl.GetCollection("Components", objZooApp.Key) 

    '  Find the Dog component item in this "Components" collection.
    '  First Populate the collection to read in data for all its items. 
    objZooComponentsColl.Populate

    '  Enumerate through the "Components" collection 
    '  until the Dog component item is located. 
    Dim objDog As COMAdminCatalogObject 
    For Each objDog in objZooComponentsColl
        If objDog.Name = "Dog" Then 
            Exit For
        End If
    Next 
    '  Set the role checking property at the component level for Dog.
        objDog.Value("ComponentAccessChecksEnabled") = True 

    '  Save these changes.
        objZooComponentsColl.SaveChanges
    '  Get the "RolesForComponent" collection related to the 
    '  Dog component, using the Key property of objDog. 
    Dim objRolesForDogColl As COMAdminCatalogCollection 
    Set objRolesForDogColl = objZooComponentsColl.GetCollection("RolesForComponent", objDog.Key) 

    '  Add a new item to this "RolesForComponent" collection. 
    Dim objCatSneezerRole As COMAdminCatalogObject
    Set objCatSneezerRole = objRolesForDogColl.Add

    '  Set the "Name" of the new item to be "AllergicToCats". 
    objCatSneezerRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to this "RolesForComponent" collection. 
    objRolesForDogColl.SaveChanges

    '  Now set properties to enforce role-based security. 
    '  First set role-based security at the application level.
    objZooApp.Value("ApplicationAccessChecksEnabled") = True 
    objZooApp.Value("AccessChecksLevel") = COMAdminAccessChecksApplicationComponentLevel 

    '  Save these changes.
    objApplicationsColl.SaveChanges

    '  Finally, export the new configured MyHomeZoo application to an 
    '  MSI file, used to install the application on other machines.
    '  Use the ExportApplication method on COMAdminCatalogObject.
    objCatalog.ExportApplication "MyHomeZoo", "c:\Program Files\COM applications\MyHomeZoo.MSI", 4

    '  Exit the function gracefully.
    SetupMyZoo = True

My_Error_Handler:
    If Not SetupMyZoo Then
        MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) & ")" & vbNewLine & Err.Description
    End If
    objCatSneezerRole = Nothing
    objRolesForDogColl = Nothing
    objDog = Nothing
    objZooComponentsColl = Nothing
    objAllergicToCatsRole = Nothing
    objZooKeeperRole = Nothing
    objRolesColl = Nothing
    objZooApp = Nothing
    objApplicationsColl = Nothing
    objCatalog = Nothing
Exit Function
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Opérations d’administration COM+ dans les transactions](com--administration-operations-within-transactions.md)
</dt> <dt>

[Gestion des erreurs d’administration COM+](handling-com--administration-errors.md)
</dt> <dt>

[Vue d’ensemble des objets comadmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Récupération des regroupements sur le catalogue COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Définition des propriétés et enregistrement des modifications dans le catalogue COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



