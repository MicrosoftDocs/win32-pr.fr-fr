---
description: Une extension de composant logiciel enfichable d’une pièce jointe doit s’ajouter elle-même sous le nœud services lorsque ce nœud est développé par un utilisateur.
ms.assetid: af853c29-11c2-4fd0-ad81-80aebeb74cc3
title: Ajout d’un nœud d’extension de composant logiciel enfichable pièce jointe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2604a58284af7bc55ff57ae114bc77d8f0cd42ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120774"
---
# <a name="adding-an-attachment-snap-in-extension-node"></a>Ajout d’un nœud d’extension de composant logiciel enfichable pièce jointe

Une extension de composant logiciel enfichable d’une pièce jointe doit s’ajouter elle-même sous le nœud services lorsque ce nœud est développé par un utilisateur.

Lorsqu’un utilisateur développe le nœud services sous l’un des composants logiciels enfichables de configuration de sécurité, MMC utilise [**IComponentData :: Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) et le \_ message de notification MMCN Expand pour notifier le composant logiciel enfichable Configuration de la sécurité, ainsi que toutes ses extensions.

Le composant logiciel enfichable Configuration de la sécurité extrait ensuite son format interne à partir du *lpDataObject*, qui est passé de l’infrastructure principale MMC en tant que type **lpDataObject**. Il arrête le traitement lorsqu’il voit le type de nœud des services. L’extension du composant logiciel enfichable d’attachement extrait ensuite le type de nœud à partir du *lpDataObject*. Si le type de nœud est l’un des types de nœuds définis du service, l’extension du composant logiciel enfichable d’attachement insère ses nœuds racine sous le nœud parent spécifié.

Notez que dans cet exemple, ExtractNodeType est une fonction privée implémentée par l’extension. L’extension examine l’objet de données pour récupérer le type de nœud. L’implémentation de ExtractNodeType n’est pas affichée.


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



 

 
