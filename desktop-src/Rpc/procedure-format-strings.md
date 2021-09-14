---
title: Chaînes de format de procédure
description: Voici une description complète de la chaîne de format. Il rassemble toutes les couches liées aux différentes étapes de l’évolution de l’interpréteur.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e58a9acf10caad23063bdba117dc402e411638
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311493"
---
# <a name="procedure-format-strings"></a>Chaînes de format de procédure

Voici une description complète de la chaîne de format. Il rassemble toutes les couches liées aux différentes étapes de l’évolution de l’interpréteur.

## <a name="procedure-descriptor-overview"></a>Vue d’ensemble du descripteur de procédure

Un descripteur de procédure se compose des descripteurs d’en-tête et des descripteurs de paramètre. La description du style [**– OI**](/windows/desktop/Midl/-oi) est considérée comme obsolète, en termes d’utilisation courante dans la programmation RPC actuelle. Le **– les interfaces** de prise en compte sont considérées comme plus actuelles.

## <a name="the-oi-style-description"></a>Description du style – OI

Cette description est constituée des éléments suivants :

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

L’en-tête doit être compris entre 6 et 16 octets.

La description complète est générée lors de la compilation en mode [**– OI**](/windows/desktop/Midl/-oi) . Dans [**– mode système d’exploitation**](/windows/desktop/Midl/-os) , seuls les descripteurs de paramètre sont générés, qui sont utilisés pour la conversion. L’interpréteur de sélection utilise les descripteurs de paramètre de style anciens.

## <a name="the-oif-style-description"></a>Description du style de-type d’interfaces

La description est constituée des éléments suivants :

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

Le descripteur d' [**en-tête**](/windows/desktop/Midl/-oi) de style

La description du style – de l’interfaces de génération est générée lors de la compilation dans le mode [**–**](/windows/desktop/Midl/-oi) **Oicf ou –** du compilateur.

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

Certaines fonctionnalités plus récentes telles que pipe, Async et [**/Robust**](/windows/desktop/Midl/-robust) forcent le mode [**– Oicf**](/windows/desktop/Midl/-oi) du compilateur, lorsqu’ils sont utilisés.

## <a name="the-extended-oif-description"></a>Description étendue – interfaces

La description est constituée des éléments suivants :

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 