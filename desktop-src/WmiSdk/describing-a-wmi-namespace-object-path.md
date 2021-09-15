---
description: Un chemin d’accès d’objet d’espace de noms décrit l’emplacement d’un espace de noms particulier sur un serveur. Un chemin d’accès à un objet d’espace de noms contient des éléments de serveur et d’espace de noms.
ms.assetid: 6d8da19e-0914-4267-870e-c203176b895e
ms.tgt_platform: multiple
title: Description d’un chemin d’accès d’objet d’espace de noms WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586104a1c193f1c229b0fbb27437d22e3686585b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411563"
---
# <a name="describing-a-wmi-namespace-object-path"></a>Description d’un chemin d’accès d’objet d’espace de noms WMI

Un chemin d’accès d’objet d’espace de noms décrit l’emplacement d’un espace de noms particulier sur un serveur. Un chemin d’accès à un objet d’espace de noms contient des éléments de serveur et d’espace de noms.

L’élément Server spécifie le nom réseau de l’ordinateur qui héberge l’espace de noms, comme indiqué dans l’exemple suivant.

``` syntax
\\Server\Namespace
```

\- ou -

``` syntax
//Server/Namespace
```

Si le serveur est l’ordinateur local, utilisez un point unique au lieu du nom du serveur, comme indiqué dans l’exemple suivant.

``` syntax
\\.\Namespace
```

L’élément namespace spécifie un espace de noms valide. Un espace de noms est représenté par une chaîne hiérarchique contenant des éléments délimités par des barres obliques inverses uniques, telles que \\ cimv2 racine. Vous ne pouvez pas utiliser les barres obliques dans les noms d’espaces de noms.

 

 



