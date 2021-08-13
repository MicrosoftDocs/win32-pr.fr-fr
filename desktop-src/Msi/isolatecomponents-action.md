---
description: L’action IsolateComponents installe une copie d’un composant (généralement une DLL partagée) dans un emplacement privé pour une utilisation par une application spécifique (en général une .exe).
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Action IsolateComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2919a026fb8243d7f2f73bc856390865ea3bed19e228da780e39f9dce68bc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629732"
---
# <a name="isolatecomponents-action"></a>Action IsolateComponents

L’action IsolateComponents installe une copie d’un composant (généralement une DLL partagée) dans un emplacement privé pour une utilisation par une application spécifique (en général une .exe). Cela isole l’application des autres copies du composant qui peuvent être installées dans un emplacement partagé sur l’ordinateur. Pour plus d’informations, consultez [composants isolés](isolated-components.md).

L’action fait référence à chaque enregistrement de la [table IsolatedComponent](isolatedcomponent-table.md) et associe les fichiers du composant figurant dans le \_ champ composant partagé avec le composant indiqué dans le \_ champ application du composant. Le programme d’installation installe les fichiers du composant \_ partagé dans le même répertoire que le composant \_ application. Le programme d’installation génère un fichier dans ce répertoire, avec une longueur de zéro octet, avec le nom de fichier Short du fichier de clé pour l’application de composant \_ (en général, il s’agit du même nom de fichier que le .exe) ajouté avec. local. L’action IsolatedComponent n’affecte pas l’installation de l' \_ application de composant. La désinstallation \_ de l’application de composant supprime également les \_ fichiers partagés du composant et le fichier. local du répertoire.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action IsolateComponents ne peut être utilisée que dans la [table InstallUISequence](installuisequence-table.md) et la [table InstallExecuteSequence](installexecutesequence-table.md). Cette action doit être postérieure à l’action [CostInitialize](costinitialize-action.md) et avant l' [action CostFinalize](costfinalize-action.md).

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Remarques

Si la colonne condition de l’action IsolateComponents prend la valeur true ou si elle est laissée vide, le programme d’installation isole tous les composants listés dans la [table IsolatedComponent](isolatedcomponent-table.md). Si la colonne condition prend la valeur false, le programme d’installation ignore la table IsolatedComponent et partage les composants normalement. La propriété [**RedirectedDllSupport**](redirecteddllsupport.md) peut être utilisée pour conditionner cette action. Pour plus d’informations, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

 

 



