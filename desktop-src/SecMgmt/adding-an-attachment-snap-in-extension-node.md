---
description: Une extension de composant logiciel enfichable d’une pièce jointe doit s’ajouter elle-même sous le nœud services lorsque ce nœud est développé par un utilisateur.
ms.assetid: af853c29-11c2-4fd0-ad81-80aebeb74cc3
title: Ajout d’un nœud d’extension de composant logiciel enfichable pièce jointe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2604a58284af7bc55ff57ae114bc77d8f0cd42ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758037"
---
# <a name="adding-an-attachment-snap-in-extension-node"></a><span data-ttu-id="9851d-103">Ajout d’un nœud d’extension de composant logiciel enfichable pièce jointe</span><span class="sxs-lookup"><span data-stu-id="9851d-103">Adding an Attachment Snap-in Extension Node</span></span>

<span data-ttu-id="9851d-104">Une extension de composant logiciel enfichable d’une pièce jointe doit s’ajouter elle-même sous le nœud services lorsque ce nœud est développé par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9851d-104">An attachment snap-in extension must add itself under the Services node when that node is expanded by a user.</span></span>

<span data-ttu-id="9851d-105">Lorsqu’un utilisateur développe le nœud services sous l’un des composants logiciels enfichables de configuration de sécurité, MMC utilise [**IComponentData :: Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) et le \_ message de notification MMCN Expand pour notifier le composant logiciel enfichable Configuration de la sécurité, ainsi que toutes ses extensions.</span><span class="sxs-lookup"><span data-stu-id="9851d-105">When a user expands the Services node under one of the Security Configuration snap-ins, MMC uses [**IComponentData::Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) and the MMCN\_EXPAND notification message to notify the Security Configuration snap-in, plus all its extensions.</span></span>

<span data-ttu-id="9851d-106">Le composant logiciel enfichable Configuration de la sécurité extrait ensuite son format interne à partir du *lpDataObject*, qui est passé de l’infrastructure principale MMC en tant que type **lpDataObject**.</span><span class="sxs-lookup"><span data-stu-id="9851d-106">The Security Configuration snap-in then extracts its internal format from the *lpDataObject*, which is passed in from the MMC main framework as type **LPDATAOBJECT**.</span></span> <span data-ttu-id="9851d-107">Il arrête le traitement lorsqu’il voit le type de nœud des services.</span><span class="sxs-lookup"><span data-stu-id="9851d-107">It stops processing when it sees the Services node type.</span></span> <span data-ttu-id="9851d-108">L’extension du composant logiciel enfichable d’attachement extrait ensuite le type de nœud à partir du *lpDataObject*.</span><span class="sxs-lookup"><span data-stu-id="9851d-108">The attachment snap-in extension then extracts the node type from the *lpDataObject*.</span></span> <span data-ttu-id="9851d-109">Si le type de nœud est l’un des types de nœuds définis du service, l’extension du composant logiciel enfichable d’attachement insère ses nœuds racine sous le nœud parent spécifié.</span><span class="sxs-lookup"><span data-stu-id="9851d-109">If the node type is one of the service's defined node types, the attachment snap-in extension inserts its root nodes under the specified parent node.</span></span>

<span data-ttu-id="9851d-110">Notez que dans cet exemple, ExtractNodeType est une fonction privée implémentée par l’extension.</span><span class="sxs-lookup"><span data-stu-id="9851d-110">Note that in this example, ExtractNodeType, is a private function that the extension implements.</span></span> <span data-ttu-id="9851d-111">L’extension examine l’objet de données pour récupérer le type de nœud.</span><span class="sxs-lookup"><span data-stu-id="9851d-111">The extension examines the data object to get the node type.</span></span> <span data-ttu-id="9851d-112">L’implémentation de ExtractNodeType n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="9851d-112">The implementation of ExtractNodeType is not shown.</span></span>


```C++
//  Detect which extension node to expand.
GUID* nodeType = ExtractNodeType(lpdataObject);

if (NULL == nodeType)
{
  return S_OK;
}

if (TRUE == ::IsEqualGUID(*nodeType, cNodetypeSceTemplateServices))
{
  folderType = ATTACHMENT_STATIC;  // defined by attachment writer
}

else if (TRUE == ::IsEqualGUID
    (*nodeType, cNodetypeSceAnalysisServices))
{
  folderType = ATTACHMENT_STATIC_ANALYSIS;
               // defined by attachment writer
}

//  Free resources.
::GlobalFree(reinterpret_cast<HANDLE>(nodeType));

//  Add service attachment root node and remember it as the
//  root of the SMB extension namespace.
//  ...
```



 

 
