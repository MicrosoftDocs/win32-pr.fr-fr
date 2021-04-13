---
title: Événement BalloonShow
description: Événement BalloonShow
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de67318b02775619332fe60ea47fb27edb893c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380206"
---
# <a name="balloonshow-event"></a>Événement BalloonShow

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque la bulle de texte d’un caractère est affichée.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sub** *agent* \_ **BalloonShow** **(ByVal** *CharacterID * * *)**



| Partie          | Description                                                       |
|---------------|-------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère associé au mot-bulle. |



 

</dd> </dl>

### <a name="remarks"></a>Notes

Le serveur envoie cet événement uniquement aux clients du caractère (applications qui ont chargé le caractère) qui utilise le mot-bulle.

### <a name="see-also"></a>Voir aussi

[**Événement BalloonHide**](balloonhide-event.md)


 

 




