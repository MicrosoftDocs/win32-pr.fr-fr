---
description: Alors que les fournisseurs de services Windows Sockets sont encouragés à implémenter des sockets en tant qu’objets IFS (Installable File System), l’architecture Winsock prend également en charge les fournisseurs de services dont les handles de socket ne sont pas des objets IFS.
ms.assetid: ed5e10f4-fa17-4a07-9cac-43767915b8e9
title: Allocation du descripteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095301798eb850fc4eb63e1939712379b5ead85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514180"
---
# <a name="descriptor-allocation"></a>Allocation du descripteur

Alors que les fournisseurs de services Windows Sockets sont encouragés à implémenter des sockets en tant qu’objets IFS (Installable File System), l’architecture Winsock prend également en charge les fournisseurs de services dont les handles de socket ne sont pas des objets IFS. Les fournisseurs avec des handles IFS l’indiquent par le biais du \_ \_ bit de l’attribut XP1 IFS handles dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . (Remarque : XP1 \_ IFS \_ gère le bit d’attribut n’a pas été inclus dans la version 2.0.8 de la spécification de l’API, mais a été ajouté par le biais du mécanisme errata.) Les clients Winsock SPI peuvent tirer parti des fournisseurs dont les descripteurs de socket sont des descripteurs IFS en utilisant ces descripteurs avec les fonctionnalités d’e/s Windows standard, telles que [ReadFile](/windows/win32/api/fileapi/nf-fileapi-readfile) et [WriteFile](/windows/win32/api/fileapi/nf-fileapi-writefile).

Chaque fois qu’un fournisseur IFS crée un descripteur de socket, il est obligatoire que le fournisseur appelle [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) avant de fournir le nouveau descripteur à un client SPI Windows Sockets. Cette fonction prend un identificateur de fournisseur et un handle IFS proposé du fournisseur comme entrée et retourne un handle (éventuellement) modifié. Le fournisseur IFS ne doit fournir que le descripteur modifié à son client, et toutes les demandes du client référencent uniquement ce handle modifié. Il est garanti que le descripteur modifié ne peut pas être distingué du handle proposé en ce qui concerne le système d’exploitation. Par conséquent, dans la plupart des cas, le fournisseur de services choisira simplement d’utiliser uniquement le descripteur modifié dans tout son traitement interne. L’objectif de cette fonction de modification est de permettre à l'32.dll Ws2 de \_ simplifier considérablement le processus d’identification du fournisseur de services associé à un socket donné.

Les fournisseurs qui ne retournent pas de handles IFS doivent obtenir un handle valide de la \_32.dll Ws2 via l’appel [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) . Le fournisseur nonIFS doit proposer uniquement un handle Windows Sockets fourni par 2.DLL à son client, et toutes les demandes du client référencent uniquement ces handles. Pour faciliter l’implémentation des fournisseurs de services, l’un des paramètres d’entrée fournis par un fournisseur dans **WPUCreateSocketHandle** est une valeur de contexte DWORD. Le \_32.dll Ws2 associe cette valeur de contexte au handle de socket alloué et permet à un fournisseur de services de récupérer la valeur de contexte à tout moment via l’appel [**WPUQuerySocketHandleContext**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuquerysockethandlecontext) . Une utilisation courante de cette valeur de contexte serait de stocker un pointeur vers une structure de données gérée par le fournisseur de services utilisée pour stocker les informations d’État du Socket.

 

 
