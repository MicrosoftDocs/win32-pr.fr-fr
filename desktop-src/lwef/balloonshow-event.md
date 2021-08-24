---
title: Événement BalloonShow
description: Événement BalloonShow
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10aa8ab2c556fdf603a3972033a7440041fef6a45f828115c649a8a42810eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726139"
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

### <a name="remarks"></a>Remarques

Le serveur envoie cet événement uniquement aux clients du caractère (applications qui ont chargé le caractère) qui utilise le mot-bulle.

### <a name="see-also"></a>Voir aussi

[**Événement BalloonHide**](balloonhide-event.md)


 

 




