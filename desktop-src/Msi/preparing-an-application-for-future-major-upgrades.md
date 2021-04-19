---
description: Les auteurs des packages d’installation doivent inclure des informations de mise à niveau dans leurs fichiers. msi pour s’assurer que leur package d’installation peut tirer parti de la fonctionnalité de mise à niveau complète disponible avec la Microsoft Windows Installer.
ms.assetid: 88bb2709-a1bf-4140-a145-ae6bee85dde1
title: Préparation d’une application pour les futures mises à niveau majeures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e0dc9ccbee10becc39274e91d2fedeb3707028
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524173"
---
# <a name="preparing-an-application-for-future-major-upgrades"></a>Préparation d’une application pour les futures mises à niveau majeures

Les auteurs des packages d’installation doivent inclure des informations de mise à niveau dans leurs fichiers. msi pour s’assurer que leur package d’installation peut tirer parti de la fonctionnalité de mise à niveau complète disponible avec la Microsoft Windows Installer.

Chaque application ou suite d’applications doit être assignée à la propriété [**UpgradeCode**](upgradecode.md) , à la propriété [**ProductVersion**](productversion.md) et à la propriété [**ProductLanguage**](productlanguage.md) . La propriété [**UpgradeCode**](upgradecode.md) indique une famille d’applications associées qui se composent de versions différentes et de différentes versions linguistiques du même produit. Pour plus d’informations sur l’utilisation de la propriété [**UpgradeCode**](upgradecode.md) , consultez [utilisation d’une UpgradeCode](using-an-upgradecode.md).

**Préparation d’une application pour les futures mises à niveau majeures**

1.  Déterminez une nouvelle valeur de code de package pour l’application. Pour plus d’informations sur les codes de package, consultez [codes de package](package-codes.md). Entrez le nouveau code de package dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) du flux d’informations de [synthèse](summary-information-stream.md).
2.  Déterminez une nouvelle propriété [**ProductCode**](productcode.md) pour l’application. Pour plus d’informations, consultez [modification du code du produit](changing-the-product-code.md) . Entrez [**ProductCode**](productcode.md) et sa valeur dans la [table de propriétés](property-table.md).
3.  Déterminez la version de l’application et la propriété [**ProductVersion**](productversion.md) . Le [**ProductVersion**](productversion.md) doit augmenter avec chaque nouvelle version de l’application. Notez que le programme d’installation utilise uniquement les trois premiers champs de la version du produit. Si vous incluez un quatrième champ dans la version de votre produit, le programme d’installation ignore le quatrième champ. Entrez [**ProductVersion**](productversion.md) et sa valeur dans la table de propriétés.
4.  Déterminez la langue du package et la propriété [**ProductLanguage**](productlanguage.md) . La valeur de cette propriété doit être un identificateur de langue numérique (LANGID). Entrez [**ProductLanguage**](productlanguage.md) et sa valeur dans la [table de propriétés](property-table.md). Notez que l' [action FindRelatedProducts](findrelatedproducts-action.md) utilise la langue retournée par [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa). Pour que FindRelatedProducts fonctionne correctement, l’auteur du package doit s’assurer que la propriété [**ProductLanguage**](productlanguage.md) est définie dans la table de propriétés sur une langue qui est également indiquée dans la propriété [**Résumé du modèle**](template-summary.md) .
5.  Si vous créez un package d’installation pour la première version de votre produit, utilisez une nouvelle [**UpgradeCode**](upgradecode.md). Si votre package est destiné à une version plus récente d’un produit existant, ou s’il s’agit de la même version qu’un produit existant dans une autre langue, utilisez la même [**UpgradeCode**](upgradecode.md) que le produit existant. Deux produits avec le même [**ProductVersion**](productversion.md) et le même [**ProductLanguage**](productlanguage.md) ne peuvent pas avoir le même [**UpgradeCode**](upgradecode.md), sauf s’il s’agit d’une [petite mise à jour](small-updates.md) de l’autre.
6.  La [**UpgradeCode**](upgradecode.md) a le format d’un [GUID](guid.md). Entrez le GUID de [**UpgradeCode**](upgradecode.md) dans la table de propriétés.

Pour plus d’informations, consultez [la page empêcher l’installation d’un ancien package sur une version plus récente](preventing-an-old-package-from-installing-over-a-newer-version.md).

 

 



