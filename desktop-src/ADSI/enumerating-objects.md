---
title: Énumération d’objets
description: Pour afficher l’objet enfant d’un conteneur, tel qu’une unité d’organisation (UO), énumérez l’objet conteneur.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Énumération d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e4bcead2d3fc8f98daeada89cdd10b3ad30bed855563efd89b3eebce8995f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961948"
---
# <a name="enumerating-objects"></a>Énumération d’objets

Pour afficher l’objet enfant d’un conteneur, tel qu’une unité d’organisation (UO), énumérez l’objet conteneur. Pour effectuer une analogie avec un système de fichiers, l’objet enfant correspond aux fichiers du répertoire, tandis que le conteneur, qui est l’objet parent, correspond au répertoire lui-même. Vous pouvez également utiliser l’opération d’énumération lorsque vous souhaitez obtenir l’objet parent d’un objet.

Quand vous énumérez un objet, vous vous liez en fait à un objet dans le répertoire, et une interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) est retournée sur chaque objet.

L’exemple de code suivant montre comment énumérer les enfants d’un conteneur.


```VB
Dim ou As IADs
' Bind to an object using its DN.
On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")

For each child in ou
    Debug.Print child.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
```



Vous pouvez filtrer les types d’objets retournés à partir de l’énumération. Par exemple, pour afficher uniquement les utilisateurs et les groupes, utilisez l’exemple de code suivant avant l’énumération.


```VB
Ou.Filter = Array("user", "group")
```



Si vous disposez d’une référence d’objet, vous pouvez obtenir le parent de l’objet à l’aide de la propriété [**parente**](iads-property-methods.md) [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . L’exemple de code suivant montre comment effectuer une liaison à l’objet parent.


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



Pour plus d’informations, consultez [énumération des objets ADSI](enumerating-adsi-objects.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche d’objets](searching-for-objects.md)
</dt> </dl>

 

 




