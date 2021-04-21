---
title: Historique des versions DirectML
description: DirectML est distribué en tant que composant système de Windows 10 et est disponible dans le cadre du système d’exploitation Windows 10 (se) dans Windows 10, version 1903 (10,0 ; Build 18362) et versions ultérieures.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: f5e0a478b2d4c6728a1cd53388ba09af8e5bbc0e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803937"
---
# <a name="directml-version-history"></a>Historique des versions DirectML

DirectML est distribué en tant que composant système de Windows 10 et est disponible dans le cadre du système d’exploitation Windows 10 (se) dans Windows 10, version 1903 (10,0 ; Build 18362) et versions ultérieures.

À compter de DirectML version 1.4.0, DirectML est également disponible en tant que package redistribuable autonome (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)), ce qui est utile pour les applications qui souhaitent utiliser une version fixe de DirectML, ou lorsqu’elles s’exécutent sur des versions antérieures de Windows 10.

DirectML suit les conventions de contrôle de [version sémantique](https://semver.org/) . Autrement dit, les numéros de version suivent le formulaire `major.minor.patch` . La première version de DirectML a une version de 1.0.0.

## <a name="version-table"></a>Table de version

|Version de DirectML|Niveau de fonctionnalité pris en charge (voir [l’historique des niveaux de fonctionnalité DirectML](./dml-feature-level-history.md))|DML_TARGET_VERSION|Tout d’abord disponible dans|Tout d’abord disponible dans (redistribuable)|
|-|-|-|-|-|-|
|1.5.0|DML_FEATURE_LEVEL_3_1|`0x3100`|N/A|[DirectML-1.5.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.5.0)|
|1.4.0<sup>1</sup>|DML_FEATURE_LEVEL_3_0|`0x3000`|N/A|[DirectML-1.4.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.4.0)|
|1.1.0|DML_FEATURE_LEVEL_2_0|`0x2000`|Windows 10, version 2004 (10,0 ; Build 19041) (Windows 10 mai 2020 Update). Alias « 20H1 ».|N/A|
|1.0.0|DML_FEATURE_LEVEL_1_0|`0x1000`|Windows 10, version 1903 (10,0 ; Build 18362) (Windows 10 mai 2019 Update). Alias « 19H1 ».|N/A|

<sup>1</sup> les versions intermédiaires 1.2.0 et 1.3.0 de DirectML n’ont pas été mises à la disposition large.

## <a name="selecting-a-directml-target-version"></a>Sélection d’une version cible de DirectML

Pour plus de commodité, certaines fonctionnalités du `DirectML.h` fichier d’en-tête sont déclarées conditionnellement en fonction de la valeur de la `DML_TARGET_VERSION` macro. En définissant la `DML_TARGET_VERSION` macro sur certaines valeurs, vous pouvez exclure des parties de de `DirectML.h` votre application.

Cela peut être utile si vous utilisez une copie plus récente de `DirectML.h` , mais que vous ciblez une version antérieure du fichier binaire DirectML, car cela garantit que toute tentative d’utilisation de fonctionnalités au-delà du niveau cible choisi n’est pas compilée. Ce mécanisme est similaire à la `NTDDI_VERSION` macro (consultez [macros pour les déclarations conditionnelles](../winprog/using-the-windows-headers.md#macros-for-conditional-declarations)).

Voici les valeurs valides pour la `DML_TARGET_VERSION` macro.

|DML_TARGET_VERSION|Résultat|
|-|-|
|`0x3000`|Toutes les fonctionnalités qui requièrent une version de DirectML plus récente que **1.4.0** sont exclues de `DirectML.h` .|
|`0x2000`|Toutes les fonctionnalités qui requièrent une version de DirectML plus récente que **1.1.0** sont exclues de `DirectML.h` .|
|`0x1000`|Toutes les fonctionnalités qui requièrent une version de DirectML plus récente que **1.0.0** sont exclues de `DirectML.h` .|
|*Non défini*|La version cible est sélectionnée automatiquement pour vous. Voir les détails ci-dessous.|

Si `DML_TARGET_VERSION` n’est pas défini, il est sélectionné automatiquement par les éléments suivants.

* Si la `DML_TARGET_VERSION_USE_LATEST` macro est définie, la dernière version cible est sélectionnée.
* Dans le cas contraire, la version cible est sélectionnée en fonction de la valeur de la `NTDDI_VERSION` macro.
  *  `NTDDI_WIN10_19H1` produit une version cible de `0x1000` .
  *  `NTDDI_WIN10_VB` produit une version cible de `0x2000` .
  *  Si `NTDDI_VERSION` n’est pas défini, la dernière version cible est sélectionnée (comme si `DML_TARGET_VERSION_USE_LATEST` a été spécifié).

### <a name="example"></a>Exemple

Prenons l’exemple d’une application qui utilise la version 10.0.19041.0 (Windows 10, version 2004) du kit de développement logiciel (SDK) Windows. Dans le tableau ci-dessus, la version de DirectML qui correspond à est 1.1.0 et le correspondant `DML_TARGET_VERSION` est `0x2000` .

Si vous ne définissez pas les `DML_TARGET_VERSION` `NTDDI_VERSION` macros et, la version cible sélectionnée est définie par défaut sur `0x2000` , et tout ce qui est `DirectML.h` disponible peut être utilisé.

Si vous souhaitez que votre application soit en mesure de s’exécuter sur Windows 10, version 1903 (10,0 ; Build 18362). vous pouvez alors `#define DML_TARGET_VERSION 0x1000` exclure tout le contenu dans `DirectML.h` qui n’est pas pris en charge par DirectML version 1.0.0. Cela garantit que toute tentative d’utilisation d’une fonctionnalité nécessitant une version supérieure échouera à se compiler.

## <a name="directml-version-versus-feature-level"></a>Version de DirectML et niveau de fonctionnalité

La version de DirectML (par exemple, 1.0.0 ou 1.4.0) décrit une version particulière de DirectML, y compris son `DirectML.h` fichier d’en-tête et son fichier d’en-tête associés `.lib` .

Le niveau de fonctionnalité (par exemple, `DML_FEATURE_LEVEL_1_0` ou `DML_FEATURE_LEVEL_2_0` ) décrit la capacité de l’implémentation sous-jacente de l’API, qui peut varier de la version de `DirectML.h` utilisée.

Par exemple, une application qui s’exécute sur un kit de développement logiciel (SDK) plus récent, mais qui s’exécute sur une version antérieure de Windows, peut (au moment de l’exécution) Voir un niveau de fonctionnalité pris en charge inférieur, même s’il est compilé avec le dernier Kit de développement logiciel (SDK).

## <a name="see-also"></a>Voir aussi

* [Historique des niveaux de fonctionnalité DirectML](./dml-feature-level-history.md)
* [Énumération DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Package redistribuable Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)