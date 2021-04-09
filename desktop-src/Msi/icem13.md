---
description: ICEM13 vérifie que le module de fusion ne contient pas d’assemblys de stratégie et de configuration d’éditeur.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286906cf162f24dce7105835544c3a387993ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864405"
---
# <a name="icem13"></a>ICEM13

ICEM13 vérifie que le module de fusion ne contient pas d’assemblys de stratégie et de configuration d’éditeur. Les assemblys de stratégie et de configuration d’éditeur ne doivent pas être inclus dans les modules de fusion destinés à la redistribution, car cela peut affecter d’autres applications sur l’ordinateur d’un utilisateur.

Ce ICEM est disponible dans le fichier Mergemod. CUB fourni dans le kit de développement logiciel (SDK) Windows Installer 2,0 et versions ultérieures. Pour plus d’informations, consultez [SDK Windows Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Résultats

ICEM13 publie un message d’avertissement s’il trouve un composant spécifié dans le champ composant de la [table MsiAssembly](msiassembly-table.md) du module de fusion qui est une stratégie ou un assembly de configuration d’éditeur.

## <a name="example"></a>Exemple

ICEM13 publie le message d’avertissement suivant s’il trouve une ligne de la [table MsiAssembly](msiassembly-table.md) avec le composant « \[ 1 \] » spécifié dans le champ de composant qui est une stratégie d’éditeur ou un assembly de configuration qui a été inclus dans le module de fusion.

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

Il est possible d’installer des assemblys de stratégie et de configuration d’éditeur à l’aide de la Windows Installer, il n’est pas recommandé de redistribuer ces assemblys dans des modules de fusion.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



