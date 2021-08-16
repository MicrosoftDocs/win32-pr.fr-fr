---
description: Si cette stratégie système par ordinateur est définie sur &\# 0034 ; 1&\# 0034 ;, le programme d’installation écrit des messages de débogage communs dans le débogueur à l’aide de la fonction OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3216b863953faa7edf3f8146084a0ec794f171482e0e619d717447ca0a0f30d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692869"
---
# <a name="debug"></a>Débogage

Si cette [stratégie système](system-policy.md) par ordinateur est définie sur « 1 », le programme d’installation écrit des messages de débogage communs dans le débogueur à l’aide de la fonction [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) . Si cette valeur est définie sur « 2 », le programme d’installation écrit tous les messages de débogage valides dans le débogueur à l’aide de la fonction [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) . cette stratégie est à des fins de débogage uniquement et peut ne pas être prise en charge dans les futures versions de Windows Installer.

Windows Le programme d’installation écrit uniquement des lignes de commande dans le fichier journal si le troisième bit (0x04) est défini dans la valeur de la stratégie de débogage. Par conséquent, pour afficher les lignes de commande dans le journal, définissez la valeur de la stratégie de débogage sur 7. Cela n’affiche pas les propriétés associées à un [contrôle d’édition](edit-control.md) avec l' [attribut de contrôle de mot de passe](password-control-attribute.md). Cela rendra les propriétés définies sur la ligne de commande visibles dans le journal même si la propriété est incluse dans la propriété [**MsiHiddenProperties**](msihiddenproperties.md) . Pour plus d’informations, consultez [la page empêcher l’écriture d’informations confidentielles dans le fichier journal](preventing-confidential-information-from-being-written-into-the-log-file.md).

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

 

 
