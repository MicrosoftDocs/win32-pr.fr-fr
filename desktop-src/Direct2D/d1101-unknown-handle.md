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
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "106541803"
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

 

 




