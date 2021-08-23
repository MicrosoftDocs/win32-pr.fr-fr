---
title: Événement IdleStart
description: Événement IdleStart
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81458d4c88bc5db4ae4231ecb4ca47f456700917f42d6ccdfe5a6013bc288849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716049"
---
# <a name="idlestart-event"></a>Événement IdleStart

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque le serveur définit un caractère à l’état **ralenti** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sous** - *agent * * * \_ IdleStart* *  **(ByVal** *CharacterID * * *)**



| Partie          | Description                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère ralenti sous la forme d’une chaîne. |



 

</dd> </dl>

### <a name="remarks"></a>Remarques

Le serveur envoie cet événement à tous les clients du caractère.

### <a name="see-also"></a>Voir aussi

[**Événement IdleComplete**](idlecomplete-event.md)


 

 




