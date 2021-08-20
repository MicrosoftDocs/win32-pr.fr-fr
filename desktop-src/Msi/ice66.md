---
description: ICE66 utilise les tables de la base de données pour déterminer le schéma que votre base de données doit utiliser.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023450a451a412c47c21904ab96a13e4513c71f8327966dffa5b657b1b65bb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787399"
---
# <a name="ice66"></a>ICE66

ICE66 utilise les tables de la base de données pour déterminer le schéma que votre base de données doit utiliser.

certaines fonctionnalités peuvent uniquement être disponibles si le package est installé sur un système avec une version actuelle de Windows Installer.

## <a name="result"></a>Résultat

ICE66 publie un avertissement si votre base de données utilise un schéma incorrect.

## <a name="example"></a>Exemples

ICE66 signale l’avertissement suivant pour l’exemple indiqué.

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

cet avertissement peut être ignoré si vous souhaitez que votre package soit installé à l’aide d’une version actuelle de Windows Installer. Par exemple, si vous souhaitez que votre package soit installé uniquement sur la version 2,0 ou ultérieure, remplacez votre schéma de package (PID \_ PageCount) par 200.

[Table IsolatedComponent](isolatedcomponent-table.md)



| Composant \_ partagé | Application de composant \_ |
|-------------------|------------------------|
| Composant1        | Component2             |



 

[Flux d’informations de synthèse](summary-information-stream.md)



| PIDt           | Valeur |
|----------------|-------|
| PID \_ PageCount | 100   |



 

## <a name="table-used-during-execution"></a>Table utilisée lors de l’exécution :

[\_Table colonnes](-columns-table.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



