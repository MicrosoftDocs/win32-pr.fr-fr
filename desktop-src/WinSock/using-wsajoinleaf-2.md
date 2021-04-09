---
description: Comme mentionné précédemment, la fonction WSAJoinLeaf est utilisée pour joindre un nœud terminal dans une session multipoint.
ms.assetid: eaa1593a-36eb-4d92-a3d9-91566fc0216b
title: Utilisation de WSAJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027262a117edc5541a4809481aa4607837343b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865681"
---
# <a name="using-wsajoinleaf"></a>Utilisation de WSAJoinLeaf

Comme mentionné précédemment, la fonction [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) est utilisée pour joindre un nœud terminal dans une session multipoint. **WSAJoinLeaf** a les mêmes paramètres et la même sémantique que [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) , sauf qu’il retourne un descripteur de socket (comme dans [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)) et qu’il a un paramètre *dwFlags* supplémentaire.

Le paramètre *dwFlags* est utilisé pour indiquer si le socket doit agir uniquement comme un expéditeur, uniquement comme récepteur, ou les deux. Seuls les sockets multipoint peuvent être utilisés pour les *paramètres d'* entrée dans cette fonction. Si le socket multipoint est en mode non bloquant, le descripteur de socket retourné n’est pas utilisable tant qu’une \_ indication FD Connect correspondante n’a pas été reçue. Une application racine dans une session multipoint peut appeler [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) une ou plusieurs fois pour ajouter un certain nombre de nœuds terminaux, mais au plus une demande de connexion multipoint peut être en suspens à la fois.

Le descripteur de socket retourné par [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) diffère selon que le descripteur de socket d’entrée, *s*, est une \_ racine c ou une \_ feuille c. Lorsqu’il est utilisé avec un \_ Socket racine c, le paramètre *Name* désigne un nœud terminal particulier à ajouter et le descripteur de socket retourné est un \_ Socket feuille c correspondant au nœud terminal qui vient d’être ajouté. Il n’est pas destiné à être utilisé pour l’échange de données multipoint, mais il est plutôt utilisé pour recevoir des \_ indications FD xxx (par exemple, FD \_ Close) pour la connexion qui existe à la \_ feuille c particulière. Certaines implémentations multipoint peuvent également permettre l’utilisation de ce Socket pour les conversations latérales entre la racine et un nœud terminal individuel. Une \_ indication FD Close est reçue pour ce Socket si le nœud terminal correspondant appelle [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) à supprimer de la session multipoint. De manière symétrique, l’appel de **opération closesocket** sur le \_ Socket feuille c retourné par **WSAJoinLeaf** amène le socket dans le nœud terminal correspondant à recevoir une \_ notification FD Close.

Quand [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) est appelé avec un \_ Socket feuille c, le paramètre *Name* contient l’adresse de l’application racine (pour un schéma de contrôle enraciné) ou une session multipoint existante (schéma de contrôle non enraciné) et le descripteur de socket retourné est le même que le descripteur de socket d’entrée. Dans un schéma de contrôle avec racine, l’application racine place son \_ Socket racine c en mode d’écoute en appelant [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen). La notification d' \_ acceptation FD standard est fournie lorsque le nœud terminal demande de se joindre à la session multipoint. L’application racine utilise les fonctions [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) / [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) habituelles pour admettre le nouveau nœud terminal. La valeur retournée par **Accept** ou **WSAAccept** est également un \_ descripteur de socket feuille c, comme ceux retournés par **WSAJoinLeaf**. Pour prendre en charge les schémas multipoint qui autorisent les jointures lancées à la racine et initiées par les feuilles, il est acceptable pour un \_ Socket racine c qui est déjà en mode d’écoute d’être utilisé en tant qu’entrée dans **WSAJoinLeaf**.

Une application racine multipoint est généralement chargée du démontage ordonné d’une session multipoint. Une telle application peut utiliser [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) ou [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) sur un \_ Socket racine c pour provoquer tous les \_ sockets de feuille c associés, y compris ceux retournés à partir de [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) et leurs Sockets de feuille c correspondants \_ dans les nœuds terminaux distants, pour obtenir une \_ notification FD Close.

 

 



