---
title: Énumération d’objets
description: Pour afficher l’objet enfant d’un conteneur, tel qu’une unité d’organisation (UO), énumérez l’objet conteneur.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Énumération d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26b78f084f95ac59c909b326be10d42c4a6696a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839205"
---
# <a name="enumerating-objects"></a><span data-ttu-id="6986a-104">Énumération d’objets</span><span class="sxs-lookup"><span data-stu-id="6986a-104">Enumerating Objects</span></span>

<span data-ttu-id="6986a-105">Pour afficher l’objet enfant d’un conteneur, tel qu’une unité d’organisation (UO), énumérez l’objet conteneur.</span><span class="sxs-lookup"><span data-stu-id="6986a-105">To view the child object of a container, such as an organizational unit (OU), enumerate the container object.</span></span> <span data-ttu-id="6986a-106">Pour effectuer une analogie avec un système de fichiers, l’objet enfant correspond aux fichiers du répertoire, tandis que le conteneur, qui est l’objet parent, correspond au répertoire lui-même.</span><span class="sxs-lookup"><span data-stu-id="6986a-106">To make an analogy to a file system, the child object would correspond to files in the directory, while the container, which is the parent object, would correspond to the directory itself.</span></span> <span data-ttu-id="6986a-107">Vous pouvez également utiliser l’opération d’énumération lorsque vous souhaitez obtenir l’objet parent d’un objet.</span><span class="sxs-lookup"><span data-stu-id="6986a-107">You may also use the enumerate operation when you want to get the parent object of an object.</span></span>

<span data-ttu-id="6986a-108">Quand vous énumérez un objet, vous vous liez en fait à un objet dans le répertoire, et une interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) est retournée sur chaque objet.</span><span class="sxs-lookup"><span data-stu-id="6986a-108">When you enumerate an object, you actually bind to an object in the directory, and an [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface is returned on each object.</span></span>

<span data-ttu-id="6986a-109">L’exemple de code suivant montre comment énumérer les enfants d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="6986a-109">The following code example shows how to enumerate the children of a container.</span></span>


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



<span data-ttu-id="6986a-110">Vous pouvez filtrer les types d’objets retournés à partir de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="6986a-110">You can filter the types of objects returned from the enumeration.</span></span> <span data-ttu-id="6986a-111">Par exemple, pour afficher uniquement les utilisateurs et les groupes, utilisez l’exemple de code suivant avant l’énumération.</span><span class="sxs-lookup"><span data-stu-id="6986a-111">For example, to display only users and groups, use the following code example before the enumeration.</span></span>


```VB
Ou.Filter = Array("user", "group")
```



<span data-ttu-id="6986a-112">Si vous disposez d’une référence d’objet, vous pouvez obtenir le parent de l’objet à l’aide de la propriété [**parente**](iads-property-methods.md) [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="6986a-112">If you have an object reference, you can get the object's parent using the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) [**Parent**](iads-property-methods.md) property.</span></span> <span data-ttu-id="6986a-113">L’exemple de code suivant montre comment effectuer une liaison à l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="6986a-113">The following code example shows how to bind to the parent object.</span></span>


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



<span data-ttu-id="6986a-114">Pour plus d’informations, consultez [énumération des objets ADSI](enumerating-adsi-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6986a-114">For more information, see [Enumerating ADSI Objects](enumerating-adsi-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6986a-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6986a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6986a-116">Recherche d’objets</span><span class="sxs-lookup"><span data-stu-id="6986a-116">Searching for Objects</span></span>](searching-for-objects.md)
</dt> </dl>

 

 




