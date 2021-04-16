---
title: Modification des valeurs par défaut de sécurité pour un ordinateur
description: Modification des valeurs par défaut de sécurité pour un ordinateur
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379583"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a>Modification des valeurs par défaut de sécurité pour un ordinateur

Il n’est pas recommandé de modifier les paramètres de sécurité à l’ensemble du système, car cela affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus, et peut les empêcher de fonctionner correctement. Si vous modifiez les paramètres de sécurité à l’ensemble du système pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière. Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité Process-Wide](setting-processwide-security.md).

Certaines valeurs du Registre déterminent les paramètres de sécurité des applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Vous pouvez modifier ces paramètres à l’aide de Dcomcnfg.exe.

Pour plus d'informations, voir les rubriques suivantes :

-   [Valeurs de Registre pour la sécurité System-Wide](registry-values-for-machine-wide-security.md)
-   [Définition de la sécurité System-Wide à l’aide de DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité au niveau du processus](setting-processwide-security.md)
</dt> <dt>

[Définition de la sécurité pour les applications COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




