---
description: Les éléments suivants fournissent des instances courantes des instructions conditionnelles. Pour plus d’informations, consultez syntaxe d’instruction conditionnelle.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Exemples de syntaxe d’instruction conditionnelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091305"
---
# <a name="examples-of-conditional-statement-syntax"></a>Exemples de syntaxe d’instruction conditionnelle

Les éléments suivants fournissent des instances courantes des instructions conditionnelles. Pour plus d’informations, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).

## <a name="run-action-on-removal"></a>Exécuter l’action à la suppression.

Pour plus d’informations, consultez [conditionnement des actions à exécuter pendant la suppression](conditioning-actions-to-run-during-removal.md).

## <a name="run-action-only-if-the-product-has-not-been-installed"></a>Exécuter l’action uniquement si le produit n’a pas été installé.

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a>Exécuter l’action uniquement si le produit est installé en local. Ne pas exécuter d’action sur une réinstallation.

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

Le terme « &NomFonctionnalité = 3 » signifie que l’action consiste à installer la fonctionnalité locale. Le terme «NOT ( ! NomFonctionnalité = 3)» signifie que la fonctionnalité n’est pas installée en local.

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a>Exécuter l’action uniquement si la fonctionnalité sera désinstallée.

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

Cette condition vérifie uniquement la transition de la fonctionnalité d’un état installé de local à l’État absent.

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a>Exécuter l’action uniquement si le composant a été installé en local, mais est en état de transition hors État.

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

Le terme « ? ComponetName = 3» signifie que le composant est installé en local. Le terme « $ComponentName = 2 » signifie que l’état de l’action sur le composant est absent. Le terme « $ComponentName = 4 » signifie que l’état de l’action sur le composant est exécuté à partir de la source. Notez qu’un état d’action de publication n’est pas valide pour un composant.

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a>Exécuter l’action uniquement lors de la réinstallation d’un composant.

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a>Exécuter l’action uniquement lorsqu’un correctif est appliqué.

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

Pour plus d’informations, consultez la section Notes de la page de propriétés [**patch**](patch.md) .

 

 



