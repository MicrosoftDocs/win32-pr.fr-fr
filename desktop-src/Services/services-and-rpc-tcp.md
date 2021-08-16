---
description: à partir de Windows Vista, le gestionnaire de contrôle des services (SCM) prend en charge les appels de procédure distante via le protocole de contrôle de Transmission (rpc/TCP) et les canaux nommés (rpc/NP).
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: Services et RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d4ddfe95e114a972c600c9bef44864aa99fbe4ec412312d03e08fa7d7fe15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888556"
---
# <a name="services-and-rpctcp"></a>Services et RPC/TCP

à partir de Windows Vista, le gestionnaire de contrôle des services (SCM) prend en charge les appels de procédure distante via le protocole de contrôle de Transmission (rpc/TCP) et les canaux nommés (rpc/NP). Les fonctions SCM côté client utilisent RPC/TCP par défaut.

RPC/TCP convient à la plupart des applications qui utilisent des fonctions SCM à distance, telles que l’administration à distance ou les outils de surveillance. Toutefois, pour la compatibilité et les performances, certaines applications peuvent avoir besoin de désactiver RPC/TCP en définissant les valeurs de Registre décrites dans cette rubrique.

Lorsqu’un service appelle une fonction SCM distante, le SCM côté client tente d’abord d’utiliser RPC/TCP pour communiquer avec le SCM côté serveur. si le serveur exécute une version de Windows qui prend en charge rpc/tcp et autorise le trafic rpc/tcp, la connexion rpc/TCPP est établie. si le serveur exécute une version de Windows qui ne prend pas en charge rpc/tcp, ou prend en charge rpc/tcp, mais fonctionne derrière un pare-feu qui autorise uniquement le trafic de canal nommé, la connexion rpc/tcp expire et le SCM réessaye la connexion avec RPC/NP. Cela va aboutir, mais cela peut prendre un certain temps (généralement supérieur à 20 secondes), ce qui entraîne l’affichage du blocage de la fonction [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) .

TCP ne contient pas les informations d’identification de l’utilisateur spécifiées avec une commande **net use** . Par conséquent, si RPC/TCP est activé et que **sc.exe** est utilisé pour tenter d’accéder au service spécifié, la commande peut échouer avec l’accès refusé. La désactivation de RPC/TCP côté client entraîne l’utilisation par la commande **sc.exe** d’un canal nommé qui contient les informations d’identification de l’utilisateur, de sorte que la commande s’exécute correctement. Pour plus d’informations sur la sc.exe, consultez [contrôle d’un service à l’aide de SC](controlling-a-service-using-sc.md).

> [!Note]  
> Un service ne doit pas fournir d’informations d’identification explicites à une commande **net use** , car ces informations d’identification peuvent être partagées par inadvertance en dehors des limites de service. Au lieu de cela, le service doit utiliser l' [emprunt d’identité du client](/windows/desktop/SecAuthZ/client-impersonation) pour emprunter l’identité de l’utilisateur.

 

### <a name="rpctcp-registry-values"></a>Valeurs de Registre RPC/TCP

RPC/TCP est contrôlé par les valeurs de Registre **SCMApiConnectionParam**, **DisableRPCOverTCP** et **DisableRemoteScmEndpoints** , qui se trouvent toutes sous la clé de contrôle **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\  . Toutes ces valeurs ont un type de \_ données Reg DWORD. Les procédures suivantes montrent comment utiliser ces valeurs de Registre pour contrôler RPC/TCP.

La procédure suivante décrit comment désactiver RPC/TCP côté client.

**Pour désactiver RPC/TCP côté client**

1.  Combinez la valeur de Registre **SCMApiConnectionParam** avec la valeur de masque 0x80000000.
2.  Redémarrez l’application qui appelle la fonction [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) .

La procédure suivante décrit comment désactiver TCP côté serveur.

**Pour désactiver TCP côté serveur**

1.  Définissez la valeur de Registre **DisableRPCOverTCP** sur 1.
2.  Redémarrez le serveur.

La procédure suivante décrit comment désactiver à la fois RPC/TCP et RPC/NP sur le serveur (par exemple, pour réduire la surface d’attaque).

**Pour désactiver à la fois RPC/TCP et RPC/NP sur le serveur**

1.  Définissez la valeur de Registre **DisableRemoteScmEndpoints** sur 1.
2.  Redémarrez le serveur.

La valeur de Registre **SCMApiConnectionParam** peut également être utilisée pour spécifier l’intervalle de délai d’attente RPC/TCP, en millisecondes. Par exemple, la valeur 30 000 spécifie un intervalle de délai d’attente de 30 secondes. La valeur par défaut est 21 000 (21 secondes).

 

 
