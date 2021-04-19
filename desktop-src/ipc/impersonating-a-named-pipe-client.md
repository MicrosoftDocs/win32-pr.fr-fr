---
description: L’emprunt d’identité est la capacité d’un thread à s’exécuter dans un contexte de sécurité différent de celui du processus qui possède le thread.
ms.assetid: 1bde4d4d-958e-45f4-8cdb-0572adcaa3ac
title: Emprunt de l’identité d’un client de canal nommé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586de99ae24ba9bab8b65ba4cb1a3a91922aa9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514777"
---
# <a name="impersonating-a-named-pipe-client"></a>Emprunt de l’identité d’un client de canal nommé

L' *emprunt d’identité* est la capacité d’un thread à s’exécuter dans un contexte de sécurité différent de celui du processus qui possède le thread. L’emprunt d’identité permet au thread de serveur d’effectuer des actions pour le compte du client, mais dans les limites du contexte de sécurité du client. Le client dispose généralement d’un niveau de droits d’accès inférieur. Pour plus d’informations, consultez [emprunt d’identité](/windows/desktop/SecAuthZ/client-impersonation).

Un thread de serveur de canal nommé peut appeler la fonction [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) pour supposer que le jeton d’accès de l’utilisateur est connecté à l’extrémité cliente du canal. Par exemple, un serveur de canaux nommés peut fournir l’accès à une base de données ou à un système de fichiers sur lequel le serveur de canaux dispose d’un accès privilégié. Lorsqu’un client de canal envoie une demande au serveur, ce dernier emprunte l’identité du client et tente d’accéder à la base de données protégée. Le système accorde ou refuse ensuite l’accès du serveur, en fonction du niveau de sécurité du client. Une fois le serveur terminé, il utilise la fonction [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) pour restaurer son jeton de sécurité d’origine.

Le [niveau d’emprunt d’identité](/windows/desktop/SecAuthZ/impersonation-levels) détermine les opérations que le serveur peut effectuer en usurpant l’identité du client. Par défaut, un serveur emprunte une identité au niveau de l’emprunt d’identité SecurityImpersonation. Toutefois, lorsque le client appelle la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir un handle à l’extrémité cliente du canal, le client peut utiliser l' \_ indicateur Security SQOS \_ present pour contrôler le niveau d’emprunt d’identité du serveur.

 

 
