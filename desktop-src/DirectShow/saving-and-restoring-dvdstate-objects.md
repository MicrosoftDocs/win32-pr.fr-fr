---
description: Enregistrement et restauration d’objets DvdState
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Enregistrement et restauration d’objets DvdState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9640b20bc8d763054c15331017da343ef45f3c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515528"
---
# <a name="saving-and-restoring-dvdstate-objects"></a>Enregistrement et restauration d’objets DvdState

Les objets [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) permettent aux applications d’enregistrer un instantané de la session utilisateur, y compris des informations telles que l’emplacement actuel sur le disque, le niveau parental de la personne qui consulte, les flux audio et sous-image sélectionnés, etc. Cela signifie que les utilisateurs peuvent enregistrer leur place sur un disque DVD-Video et les regarder ultérieurement.

Les applications ne peuvent pas créer d’objets DvdState. Ces objets sont créés en interne par le navigateur DVD lorsqu’une application appelle [**IDvdInfo2 :: GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate). Les objets DvdState exposent l’interface [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) pour permettre aux applications de demander certaines informations.

Dans l’exemple d’application de DVD, les fonctions **CDvdCore :: RestoreBookmark** et **CDvdCore :: SaveBookmark** montrent comment enregistrer et récupérer des objets DvdState.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



