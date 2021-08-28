---
title: Propriété IdleOn
description: Propriété IdleOn
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e08ada4d48197e3090b5fc821b0c5b9f532f47074985218019bb14be8881e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749506"
---
# <a name="idleon-property"></a>Propriété IdleOn

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit une valeur booléenne qui détermine si le serveur gère les animations d’état **ralenti** du caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). IdleOn_ *  \[  =  *booléen*\]

</dd> </dl> 

| Partie      | Description                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expression booléenne spécifiant si le serveur gère le mode inactif. **True** (par défaut) la gestion du serveur de l’état inactif est activée. <br/> **Valeur false** La gestion du serveur de l’état inactif est désactivée. <br/> |



 

## <a name="remarks"></a>Remarques

Le serveur définit automatiquement un délai d’attente après la dernière animation lue pour un caractère. Lorsque l’intervalle de ce minuteur est terminé, le serveur commence à l’état **ralenti** d’un caractère, en lisant ses animations de **ralenti** associées à intervalles réguliers. Si vous souhaitez empêcher le serveur de lire automatiquement les animations d’état **ralenti** , affectez la valeur **false** à la propriété et lisez une animation ou appelez la méthode [**Stop**](stop-method.md) . La définition de cette valeur n’affecte pas l’état actuel de l’animation du caractère.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

 

 





