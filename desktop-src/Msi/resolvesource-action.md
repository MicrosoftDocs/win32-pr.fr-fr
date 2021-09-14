---
description: L’action ResolveSource détermine l’emplacement de la source et définit la propriété SourceDir si la source n’a pas encore été résolue.
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: Action ResolveSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009653"
---
# <a name="resolvesource-action"></a>Action ResolveSource

L’action ResolveSource détermine l’emplacement de la source et définit la propriété [**SourceDir**](sourcedir.md) si la source n’a pas encore été résolue.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action ResolveSource doit venir après l' [action CostInitialize](costinitialize-action.md).

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Remarques

L’action ResolveSource doit être appelée avant d’utiliser la propriété [**SourceDir**](sourcedir.md) dans une expression. Elle doit également être appelée avant la tentative de récupération de la valeur de la propriété **SourceDir** à l’aide de [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya). L’action ResolveSource ne doit pas être exécutée quand la source n’est pas disponible, comme c’est le cas lors de la désinstallation de l’application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résilience source](source-resiliency.md)
</dt> </dl>

 

 



