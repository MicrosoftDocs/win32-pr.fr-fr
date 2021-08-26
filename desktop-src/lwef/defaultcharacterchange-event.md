---
title: Événement DefaultCharacterChange
description: Événement DefaultCharacterChange
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed166608d3f3b874e975ff58f600d24b73b50e293333b841039b2240780b4de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963129"
---
# <a name="defaultcharacterchange-event"></a>Événement DefaultCharacterChange

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque l’utilisateur modifie le caractère par défaut.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sous** - *agent. * * * DefaultCharacterChange* *  **(GUID ByVal** ** * *)**



| Partie   | Description                                      |
|--------|--------------------------------------------------|
| *GUID* | Retourne l’identificateur unique du caractère. |



 

</dd> </dl>

### <a name="remarks"></a>Remarques

Cet événement indique que l’utilisateur a modifié le caractère affecté comme caractère par défaut de l’utilisateur. Le serveur l’envoie uniquement aux clients qui ont chargé le caractère par défaut.

Lorsque le nouveau caractère apparaît, il suppose la même taille que toute instance déjà chargée du caractère ou le caractère par défaut précédent (dans cet ordre).

### <a name="see-also"></a>Voir aussi

[**Méthode ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md), [ **méthode Load**](load-method.md)


 

 




