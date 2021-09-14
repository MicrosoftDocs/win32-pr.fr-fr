---
description: sur les Windowss 64 bits, les portions des entrées de registre sont stockées séparément pour les applications 32 bits et 64 bits et mappées dans des vues de registre logique distinctes à l’aide du redirecteur du registre et de la réflexion du registre, car la version de 64 bits d’une application peut utiliser des clés de registre et des valeurs différentes de celles de la version de 32 bits. Il existe également des clés de Registre partagées qui ne sont pas redirigées ou reflétées.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: Données d’application 32 bits et 64 bits dans le registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc82dfbf9b22cf90866e13109aeea2bcdb10e27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013541"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a>Données d’application 32 bits et 64 bits dans le registre

sur les Windowss 64 bits, les portions des entrées de registre sont stockées séparément pour les applications 32 bits et 64 bits et mappées dans des vues de registre logique distinctes à l’aide du [redirecteur du registre](/windows/desktop/WinProg64/registry-redirector) et de la [réflexion du registre](/windows/desktop/WinProg64/registry-reflection), car la version de 64 bits d’une application peut utiliser des clés de registre et des valeurs différentes de celles de la version de 32 bits. Il existe également des [clés de Registre partagées](/windows/desktop/WinProg64/shared-registry-keys) qui ne sont pas redirigées ou reflétées.

Le parent de chaque nœud de Registre 64 bits est le nœud Image-Specific ou ISN. Le redirecteur du Registre dirige en toute transparence l’accès au registre d’une application vers le sous-nœud ISN approprié. Les sous-nœuds de redirection de l’arborescence du Registre sont créés automatiquement par le composant WOW64 en utilisant le nom **Wow6432Node**. Par conséquent, il est essentiel de ne pas nommer une clé de registre que vous créez **Wow6432Node**.

Les \_ indicateurs Key WOW64 \_ 64KEY et Key \_ WOW64 \_ 32KEY permettent un accès explicite à la vue de Registre 64 bits et à la vue 32 bits, respectivement. Pour plus d’informations, consultez [accès à une autre vue de Registre](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).

Pour désactiver et activer la réflexion du Registre pour une clé particulière, utilisez les fonctions [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) et [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) . Les applications doivent désactiver la réflexion uniquement pour les clés de registre qu’elles créent et ne pas tenter de désactiver la réflexion pour les clés prédéfinies, telles que **HKEY \_ local \_ machine** ou **HKEY \_ Current \_ User**. Pour déterminer quelles clés figurent dans la liste de réflexion, utilisez la fonction [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[redirecteur du Registre](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[réflexion du Registre](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
