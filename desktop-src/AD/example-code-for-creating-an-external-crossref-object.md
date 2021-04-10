---
title: Exemple de code pour la création d’un objet crossRef externe
description: Cette rubrique contient un exemple de code qui crée un objet crossRef externe.
ms.assetid: 282ca648-3bc7-4c5b-98db-1d8f2d040e3a
ms.tgt_platform: multiple
keywords:
- Active Directory exemples Active Directory, création d’un objet crossRef externe
- Active Directory des exemples Active Directory la création d’une publicité de référence externe, exemple de code
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 484fafed7e77fcd4d97c74c26acf8dfaf058dcf4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031005"
---
# <a name="example-code-for-creating-an-external-crossref-object"></a><span data-ttu-id="b0ee8-105">Exemple de code pour la création d’un objet crossRef externe</span><span class="sxs-lookup"><span data-stu-id="b0ee8-105">Example Code for Creating an External crossRef Object</span></span>

<span data-ttu-id="b0ee8-106">L’exemple de code Visual Basic suivant montre comment créer un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) externe.</span><span class="sxs-lookup"><span data-stu-id="b0ee8-106">The following Visual Basic code example shows how to create an external [**crossRef**](/windows/desktop/ADSchema/c-crossref) object.</span></span>


```VB
' CreateCrossRef()
'
' Description: Creates a crossRef object in the partitions container.
'
' Parameters:
'
' CrossRefName - Contains the name of the crossRef object.
'
' CrossRefDNSRoot - Contains the value to be set for the dNSRoot
' attribute of the crossRef object.
'
' CrossRefNCName - Contains the value to be set for the nCName 
' attribute of the crossRef object.
'

Sub CreateCrossRef(CrossRefName, _
                    CrossRefDNSRoot, _
                    CrossRefNCName)
    Dim oRootDSE As IADs
    Dim oPartitions As IADsContainer
    Dim ADsPath As String
    Dim oCrossRef As IADs

    ' Get the configurationNamingContext property from the 
    ' RootDSE object.
    Set oRootDSE = GetObject("LDAP://RootDSE")
    ADsPath = "LDAP://CN=Partitions," + 
              oRootDSE.Get("configurationNamingContext")
    
    ' Bind to the Partitions container.
    Set oPartitions = GetObject(ADsPath)
    
    ' Create the crossRef object.
    Set oCrossRef = oPartitions.Create("crossRef", 
                                       "CN=" & CrossRefName)
    
    ' Set the dNSRoot attribute.
    oCrossRef.Put "dNSRoot", CrossRefDNSRoot
    
    ' Set the nCName attribute.
    oCrossRef.Put "nCName", CrossRefNCName
    
    ' Commit the crossRef object to the directory.
    oCrossRef.SetInfo
End Sub
```



 

 