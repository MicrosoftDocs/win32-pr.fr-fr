---
description: Le masquage est une extension de l’emprunt d’identité qui permet de mieux contrôler la façon dont COM emprunte l’identité d’un client sur un proxy. Comme de nombreuses formes de sécurité WMI, vous définissez le masquage via les interfaces CoSetProxyBlanket et CoInitializeSecurity.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implémentation du masquage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac73d7aacf32a2168dc3651b82ae1ce3a977cf5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203963"
---
# <a name="implementing-cloaking"></a>Implémentation du masquage

Le masquage est une extension de l’emprunt d’identité qui permet de mieux contrôler la façon dont COM emprunte l’identité d’un client sur un proxy. Comme de nombreuses formes de sécurité WMI, vous définissez le masquage via les interfaces [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

COM fournit les formes de masquage suivantes :

-   statique

    COM établit l’identité du jeton par le thread ou le jeton de processus lors du premier appel au proxy. Si vous utilisez le masquage statique avec [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), vous définissez l’identité du proxy pendant la durée de vie du proxy.

-   Dynamique

    COM rétablit l’identité du jeton du thread ou du processus lors de chaque appel au proxy. Étant donné que COM vérifie l’identité sur chaque appel, le masquage dynamique permet un contrôle plus fin de l’identité du client. Toutefois, le masquage dynamique est moins efficace que le voilage statique.

Lorsque vous définissez le masquage conjointement avec le niveau de délégation d’emprunt d’identité, un serveur peut propager l’identité d’un client sur plusieurs serveurs, même si les serveurs sont distants. Si vous n’activez pas le masquage, COM effectue un appel à partir d’un serveur local vers un serveur distant dans le contexte du processus serveur réel.

Le masquage permet à WMI d’emprunter l’identité d’un client pour accéder aux ressources réseau locales et distantes sur plusieurs limites de l’ordinateur. WMI peut transmettre l’identité du client à des serveurs locaux et distants, comme d’autres instances distantes de WMI. Ces serveurs distants peuvent ensuite effectuer des opérations dans le contexte du client initial.

La procédure suivante décrit l’utilisation conjointe du masquage et de la délégation.

**Pour utiliser simultanément le masquage et la délégation**

1.  Définissez le service d’authentification sur Kerberos.

    Kerberos est le seul service d’authentification qui prend en charge le masquage à distance et la délégation. Cela signifie que le masquage et la délégation ne peuvent être utilisés que sur des serveurs distants.

2.  Marquez le compte de connexion du serveur comme « approuvé pour la délégation » dans les services Active Directory.
3.  Marquez le compte de connexion du client en tant que « le compte est sensible et ne peut pas être délégué » dans les services Active Directory.

Par exemple, un appel au fournisseur d’affichage, qui peut retourner des objets à partir de plusieurs instances de WMI sur plusieurs ordinateurs, peut tirer parti de la délégation et du masquage.

 

 
