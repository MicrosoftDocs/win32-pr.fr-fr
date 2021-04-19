---
description: Vous pouvez spécifier un descripteur de sécurité pour un canal anonyme quand vous appelez la fonction CreatePipe. Le descripteur de sécurité contrôle l’accès aux extrémités de lecture et d’écriture du canal.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Sécurité des canaux anonymes et droits d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02935a3b2bc5ea31d88aab3f23f23c348c054e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528345"
---
# <a name="anonymous-pipe-security-and-access-rights"></a>Sécurité des canaux anonymes et droits d’accès

La sécurité Windows vous permet de contrôler l’accès aux canaux anonymes. Pour plus d’informations sur la sécurité, consultez [modèle de contrôle d’accès](/windows/desktop/SecAuthZ/access-control-model).

Vous pouvez spécifier un [descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptors) pour un canal quand vous appelez la fonction [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) . Le descripteur de sécurité contrôle l’accès aux extrémités de lecture et d’écriture du canal. Si vous spécifiez **null**, le canal obtient un descripteur de sécurité par défaut. Les listes de contrôle d’accès dans le descripteur de sécurité par défaut pour un canal proviennent du jeton principal ou d’emprunt d’identité du créateur.

Pour récupérer le descripteur de sécurité d’un canal, appelez la fonction [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) . Pour modifier le descripteur de sécurité d’un canal, appelez la fonction [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

La fonction [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) retourne deux descripteurs au canal anonyme : un handle de lecture avec \_ accès de lecture et de synchronisation générique et un handle d’écriture avec un \_ accès d’écriture et de synchronisation générique. \_L’accès en écriture générique en lecture et générique \_ utilisent le même mappage de droits d’accès que pour les canaux nommés.

L' \_ accès en lecture générique pour un canal anonyme associe les droits de lecture des données du canal, de lecture des attributs de canal, de lecture des attributs étendus et de lecture de la liste DACL du canal.

L' \_ accès en écriture générique pour un canal anonyme combine les droits d’écriture de données sur le canal, y ajoute des données, écrit des attributs de canal, écrit des attributs étendus et lit la liste DACL du canal.

 

 
