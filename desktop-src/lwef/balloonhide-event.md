---
title: Événement BalloonHide
description: Événement BalloonHide
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197299"
---
# <a name="balloonhide-event"></a>Événement BalloonHide

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque la bulle de texte d’un caractère est masquée.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sub** *agent* \_ **BalloonHide** **(ByVal** *CharacterID * * *)**



| Partie          | Description                                                       |
|---------------|-------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère associé au mot-bulle. |



 

</dd> </dl>

### <a name="remarks"></a>Notes

Le serveur envoie cet événement uniquement aux clients du caractère (applications qui ont chargé le caractère) qui utilise le mot-bulle.

### <a name="see-also"></a>Voir aussi

[**Événement BalloonShow**](balloonshow-event.md)


 

 




