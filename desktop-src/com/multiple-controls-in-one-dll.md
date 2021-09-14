---
title: Plusieurs contrôles dans une DLL
description: Plusieurs contrôles dans une DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e11c91faa26420f37df330ad7f1d9eff4587f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126924636"
---
# <a name="multiple-controls-in-one-dll"></a>Plusieurs contrôles dans une DLL

une seule DLL. ocx peut conteneur un nombre quelconque de contrôles ActiveX, ce qui simplifie la distribution et l’utilisation d’un ensemble de contrôles connexes.

Si vous livrez plusieurs contrôles dans une même DLL, veillez à inclure le nom du fournisseur dans chaque nom de contrôle du package. Inclure les noms des fournisseurs dans chaque nom de contrôle permet aux utilisateurs d’identifier facilement les contrôles dans un package. Par exemple, si vous livrez une DLL qui implémente trois contrôles, Con1, Con2 et CON3, les noms des contrôles doivent être les suivants :

-   *Nom de votre société* Contrôle Con1

-   *Nom de votre société* Contrôle Con2

-   *Nom de votre société* Contrôle CON3

 

 




