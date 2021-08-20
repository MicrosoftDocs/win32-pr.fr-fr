---
title: Modifications apportées à la prise en charge matérielle héritée virtuel DX9
description: Modifications apportées à la prise en charge matérielle héritée virtuel DX9
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfd0b8bbb05161ffe14ff57cc5db97fe88a22bf6e64a495e2b43dd8240def82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211805"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a>Modifications apportées à la prise en charge matérielle héritée virtuel DX9

## <a name="platform"></a>Plateforme

**Clients** – Windows 8 


## <a name="description"></a>Description

Intel et AMD/ATI ne prennent plus en charge leurs composants graphiques virtuel DX9 et ne mettent pas à jour les pilotes de ces appareils pour Windows 8. En outre, ces appareils ne sont pas couverts pour Windows 8. Les derniers pilotes de ces périphériques sont ceux disponibles sur WU et sur les sites Web OEM/IHV. à partir de Vista, beaucoup de ces pilotes de version finale présentent des problèmes sur Windows 8. En outre, nVidia a récemment indiqué qu’ils ne prendront pas en charge leurs composants virtuel DX9 (Vista et plus anciens) mobiles (Notebook) pour Windows 8. Ils continuent à prendre en charge leurs composants Desktop virtuel DX9.

Toutes ces combinaisons de pilotes/parties se trouvent dans la liste de secours des logiciels d’Internet Explorer 9. Cela signifie que, pour des raisons de performances ou de stabilité, Internet Explorer 9 utilise le rendu logiciel sur ces périphériques. c’est une bonne indication que l’expérience avec les applications Windows store ne sera pas satisfaisante sur ces pilotes et parties.

## <a name="manifestation"></a>Manifestation

Comme il n’existe pas de prise en charge intégrée pour ces appareils, de nombreux utilisateurs disposant de ces éléments s’exécutent sur le pilote d’affichage de base de Microsoft. Il s’agit d’un GPU de logiciel WDDM 1,2 basé sur la distorsion, qui est en fait plus rapide que certains des composants de cette classe, par exemple, la série Intel GMA500. il prend en charge aero-glass et DWM et peut exécuter des applications Windows store.

Toutefois, il présente des limitations importantes :

-   Il ne prend pas en charge plusieurs moniteurs ou projection
-   Il ne prend pas en charge le mode veille, bien qu’il prenne en charge la mise en veille prolongée
-   Il n’autorise généralement pas la modification de la résolution d’écran

## <a name="mitigation"></a>Limitation des risques

Si, après le test, vous constatez que l’expérience utilisateur n’est pas acceptable, vous pouvez choisir de définir la configuration matérielle requise pour les produits qui excluent ces anciens composants Intel et AMD virtuel DX9. Vous pouvez également choisir d’alerter vos clients qu’ils peuvent avoir une expérience inacceptable sur ces parties.

## <a name="tests"></a>Tests

Évaluez les performances et l’expérience de ces appareils :

-   Quelle est l’expérience de la version finale du pilote disponible ?
-   Qu’est-ce que l’expérience comme sur le MSBDD ?

 

 




