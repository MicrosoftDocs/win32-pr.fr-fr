---
title: Propriété Enabled (objet Balloon)
description: En savoir plus sur la propriété d’objet Balloon activée. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d4eaa09e173d847e9dead1bbd559b59e2d12a2d40b5f1d1f989d3cf70263ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752001"
---
# <a name="enabled-property-balloon-object"></a>Propriété Enabled (objet Balloon)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne une valeur indiquant si la bulle de texte est activée pour le caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Balloon. activé_*



| Valeur     | Description              |
|-----------|--------------------------|
| **True**  | La bulle est activée.  |
| **False** | L’info-bulle est désactivée. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

La propriété **Enabled** retourne une valeur booléenne qui spécifie si la bulle est activée. L’État par défaut de la bulle de texte est défini dans le cadre de la définition d’un caractère lorsque le caractère est compilé dans l’éditeur de caractères Microsoft Agent. Si un caractère est défini pour ne pas prendre en charge la bulle de mot, cette propriété aura toujours la **valeur false** pour le caractère.

 

 




