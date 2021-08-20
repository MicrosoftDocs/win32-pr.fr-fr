---
title: Handle D1101 inconnu
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: Une interface non allouée par cette DLL lui a été passée.
keywords:
- D1101 descripteur Direct2D inconnu
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 37e84b9e5117732784267374ad9e6618e60d3b4020a6d23863b069b3b8233aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161000"
---
# <a name="d1101-unknown-handle"></a>D1101 : handle inconnu

Une interface d’interface \[  \] non allouée par cette dll lui a été passée.

## <a name="placeholders"></a>Espaces réservés

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interface*
</dt> <dd>

Adresse de l’interface.

</dd> </dl> 




 

## <a name="possible-causes"></a>Causes possibles

Utilisation des ressources non valide. La ressource créée en dehors de Direct2D est utilisée avec une fabrique Direct2D, ou les ressources créées sur une fabrique ont été utilisées avec une ressource créée par une autre fabrique.

 

 




