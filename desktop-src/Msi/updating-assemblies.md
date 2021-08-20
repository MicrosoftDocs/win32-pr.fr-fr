---
description: les informations contenues dans cette rubrique identifient les instructions recommandées pour la mise à jour des assemblys à l’aide de Windows Installer correctifs.
ms.assetid: 60c70d48-aae2-4ea5-a880-ac9e2c83c28c
title: Mise à jour des assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65467613206f3736f35852a919432b11a6761860bd0db22c6da2600c159ef0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141622"
---
# <a name="updating-assemblies"></a>Mise à jour des assemblys

les informations contenues dans cette rubrique identifient les instructions recommandées pour la mise à jour des assemblys à l’aide de Windows Installer correctifs.

Les auteurs des mises à jour d’assembly peuvent utiliser les instructions suivantes, qui s’appliquent à tous les types d’assemblys :

-   La méthode recommandée pour la mise à jour d’un assembly consiste à modifier le nom fort de l’assembly dans la [table MsiAssemblyName](msiassemblyname-table.md). La nouvelle version de l’assembly peut être fournie par un nouveau composant ou par le composant qui fournit l’ancienne version.
-   si la nouvelle version de l’assembly est fournie par le même composant, ne modifiez pas le type d’assembly d’un assembly .NET Framework à un assembly Win32, ou vice versa.
-   Si toutes les applications du système doivent utiliser l’assembly mis à jour, vous devez déployer un assembly de stratégie. Un assembly de stratégie peut rediriger les applications sur le système pour utiliser la nouvelle version de l’assembly. Les assemblys de stratégie doivent être fournis en créant un nouveau composant.
-   Windows Le programme d’installation 3,0 ou une version ultérieure est requis pour désinstaller les mises à jour d’assembly. Pour plus d’informations, consultez [Suppression de correctifs](removing-patches.md).
-   La version la plus récente de l’assembly doit contenir des versions identiques ou supérieures des fichiers des assemblys précédemment publiés.
-   Windows le programme d’installation 3,0 peut traiter les .NET Framework et les assemblys Win32 par un remplacement de fichier complet ou par une mise à jour delta plus petite. Pour plus d’informations, consultez réduction de la [taille des correctifs](reducing-patch-size.md).
-   Si votre mise à jour modifie le nom fort de l’assembly, la table [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) et la table [MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) sont obligatoires si le package de correctifs n’a pas de table [MsiPatchSequence](msipatchsequence-table.md) . La table MsiPatchOldAssemblyFile et la table MsiPatchOldAssemblyName ne sont pas requises si le package correctif contient des informations de séquencement de correctifs dans une table MsiPatchSequence.
-   Avant de publier un nouveau correctif, testez le correctif en l’appliquant à tous les correctifs précédemment publiés.

## <a name="updating-win32-assemblies"></a>Mise à jour des assemblys Win32

Lorsque vous mettez à jour des assemblys Win32, suivez les instructions ci-dessous :

-   Modifiez le nom fort du nouvel assembly qui est spécifié dans la [table MsiAssemblyName](msiassemblyname-table.md).
-   Si vous souhaitez que votre application utilise toujours la nouvelle version de l’assembly sans affecter la version de l’assembly utilisée par d’autres applications sur le système, utilisez le même composant pour contenir la nouvelle version de l’assembly que vous avez utilisée pour l’ancienne version de l’assembly. Conservez le même ID de [composant](component-table.md) dans la table des composants. Une fois votre application corrigée, elle contient uniquement une référence à la nouvelle version de l’assembly. L’ancienne version de l’assembly peut être conservée avec la nouvelle version dans le Global Assembly Cache. Cela n’affecte pas les autres applications du système qui utilisent l’ancienne version de l’assembly. Lorsque le même composant est utilisé à la fois pour les versions nouvelles et anciennes de l’assembly, votre mise à jour peut être un correctif Delta plus petit.
-   Si la nouvelle version de l’assembly n’est pas compatible avec tous les systèmes sur lesquels vous souhaitez installer votre application, vous pouvez installer les versions nouvelles et anciennes de l’assembly en tant qu’assemblys côte à côte. Pour installer les deux versions d’assembly côte à côte, créez un nouveau composant pour contenir la nouvelle version de l’assembly. L’ID de composant dans la table des [composants](component-table.md) du nouveau composant doit être différent de l’ID de composant du composant avec l’ancienne version. Une fois votre application corrigée, elle contient des références aux deux versions de l’assembly. L’application peut ensuite être dirigée vers la version compatible de l’assembly par un manifeste. Lorsque différents composants sont utilisés pour les versions nouvelles et anciennes de l’assembly, votre mise à jour utilise le remplacement de fichier complet.

## <a name="updating-net-framework-assemblies"></a>mise à jour des assemblys de .NET Framework

utilisez les instructions suivantes lorsque vous mettez à jour des assemblys .NET Framework.

-   Modifiez le nom fort du nouvel assembly qui est spécifié dans la [table MsiAssemblyName](msiassemblyname-table.md).
-   Si vous souhaitez que votre application utilise toujours la nouvelle version de l’assembly sans affecter la version de l’assembly utilisée par d’autres applications sur le système, modifiez le nom fort du nouvel assembly qui est spécifié dans la [table MsiAssemblyName](msiassemblyname-table.md)et utilisez le même composant pour contenir la nouvelle version de l’assembly que celle utilisée pour l’ancienne version de l’assembly. Conservez le même ID de [composant](component-table.md) dans la table des composants. Une fois votre application corrigée, elle contient uniquement une référence à la nouvelle version de l’assembly. L’ancienne version de l’assembly peut être conservée avec la nouvelle version dans le cache global. Cela n’affecte pas les autres applications du système qui utilisent l’ancienne version de l’assembly. Lorsque le même composant est utilisé à la fois pour les versions nouvelles et anciennes de l’assembly, votre mise à jour peut être un correctif Delta plus petit.
-   Si la nouvelle version de l’assembly n’est pas compatible avec tous les systèmes sur lesquels vous souhaitez installer votre application, vous pouvez installer les versions nouvelles et anciennes de l’assembly en tant qu’assemblys côte à côte. Pour installer les deux versions d’assembly côte à côte, modifiez le nom fort du nouvel assembly qui est spécifié dans la [table MsiAssemblyName](msiassemblyname-table.md), puis créez un nouveau composant pour contenir la nouvelle version de l’assembly. L’ID de composant dans la table des [composants](component-table.md) du nouveau composant doit être différent de l’ID de composant du composant avec l’ancienne version. Une fois votre application corrigée, elle contient des références aux deux versions de l’assembly. L’application peut ensuite être dirigée vers la version compatible de l’assembly par un manifeste. Lorsque différents composants sont utilisés pour les versions nouvelles et anciennes de l’assembly, votre mise à jour utilise le remplacement de fichier complet.
-   une mise à jour sur place remplace la copie d’un assembly .NET Framework dans le Global Assembly Cache. Ce type de mise à jour d’assembly ne change pas le nom fort de l’assembly. Seule la valeur du champ FileVersion de la [table MsiAssemblyName](msiassemblyname-table.md) est modifiée. la mise à jour sur place d’un assembly .NET Framework nécessite .NET Framework 1,1 SP1 ou une version ultérieure.
    > [!Note]  
    > Le type de mise à jour sur place remplace la copie de l’assembly dans le cache global et peut arrêter d’autres applications si la nouvelle version de l’assembly n’est pas totalement compatible avec le niveau de compatibilité descendante. La méthode recommandée pour la mise à jour d’un assembly consiste à modifier le nom fort de l’assembly dans la [table MsiAssemblyName](msiassemblyname-table.md).

     

 

 



