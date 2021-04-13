---
title: Configuration de SAP et RPC
description: Les serveurs réseau Novell NetWare utilisent le protocole SAP (Service Advertising Protocol) pour diffuser des informations sur les services disponibles sur le réseau vers d’autres appareils en réseau.
ms.assetid: 6d6ef481-fc09-4795-8954-33329912ff4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385d60168a52cbe5d31368959ec4f21d52f9ad80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2019
ms.locfileid: "104380470"
---
# <a name="configuring-sap-and-rpc"></a>Configuration de SAP et RPC

Les serveurs réseau Novell NetWare utilisent le protocole SAP (Service Advertising Protocol) pour diffuser des informations sur les services disponibles sur le réseau vers d’autres appareils en réseau. Un serveur peut envoyer une diffusion SAP toutes les 60 secondes pour informer les autres périphériques réseau des services qu’il offre. Les stations de travail utilisent des SAP pour trouver les services dont ils ont besoin sur le réseau.

Windows comprend un service d’agent SAP pour permettre aux serveurs Windows d’interagir avec les serveurs NetWare. Le service de l’agent SAP écoute les demandes SAP des clients réseau pour les services IPX qui sont installés et en cours d’exécution sur le serveur.

Le logiciel conçu pour être publié en tant que service sur le réseau au moyen d’une diffusion SAP émet les annonces SAP toutes les 60 secondes, sans avoir à installer l’agent SAP. Toutefois, pour que les clients réseau localisent rapidement un service réseau IPX, un serveur qui gère une base de données de service doit être disponible sur le réseau pour répondre à la demande d’emplacement du service. Cette base de données de service est généralement gérée par un serveur Novell NetWare ou un serveur compatible NetWare. Les services de fichiers et d’impression Microsoft pour NetWare conserveront également une base de données de service réseau IPX.

Sur un ordinateur exécutant Windows Server, si les services de passerelle pour NetWare (GSNW) sont installés, un type SAP 640 est diffusé toutes les 60 secondes par le service d’appel de procédure distante (RPC). Cette diffusion SAP se poursuivra même si l’utilisateur désactive la passerelle GSNW et le service SAP agent.

Le service RPC effectue la diffusion SAP si les services client pour NetWare (CSNW) et le service de l’agent SAP sont installés. Cette diffusion SAP se poursuivra même si l’utilisateur désactive l’agent SAP.

Par défaut, le service RPC vérifie la présence des services de passerelle pour NetWare et du service de l’agent SAP sur l’ordinateur exécutant Windows Server. L’installation des services de fichiers et d’impression pour NetWare installe un agent SAP.

Sur l’ordinateur exécutant une version cliente de Windows avec CSNW, le service RPC recherche le service de l’agent SAP. Si les services sont présents, RPC démarre son propre thread qui effectue le type de diffusion SAP 640 toutes les minutes.

> [!NOTE]
> Si vous ne souhaitez pas diffuser des diffusions SAP sur le réseau toutes les 60 secondes, vous pouvez désactiver les diffusions SAP à l’aide de l’éditeur du Registre. Un avertissement indiquant que l’utilisation incorrecte de l’éditeur du Registre peut provoquer des problèmes sérieux pouvant vous obliger à réinstaller votre système d’exploitation. Microsoft ne peut pas garantir que les problèmes résultant d'une utilisation incorrecte de l'éditeur du Registre puissent être résolus. Son utilisation est sous votre entière responsabilité. Vous devez sauvegarder le registre avant de le modifier.

 

**Pour configurer pour SAP**

1.  Exécutez l’éditeur du Registre (Regedt32.exe) et accédez à la clé suivante dans le registre :

    **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ RPC**

2.  Dans le menu **Edition** , cliquez sur **Ajouter une valeur** et utilisez l’entrée suivante :
    1.  Nom de la valeur : AdvertiseRpcService
    2.  Type de données : ENR \_ SZ
    3.  Chaîne : non
3.  Si vous n’utilisez pas pour la chaîne, la diffusion SAP RPC est désactivée. L’utilisation de la valeur Yes pour la chaîne active la diffusion RPC SAP sur.
4.  Redémarrez l’ordinateur pour que la modification du registre soit prise en compte.
    > [!NOTE]
    > Si les diffusions SAP continuent après avoir effectué ces étapes, vous souhaiterez peut-être essayer une étape de dépannage. Supprimez la valeur de chaîne **ncacn \_ SPX** dans la clé de Registre suivante :
    >
    > **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ RPC \\ ServerProtocols\\**

     

> [!NOTE]  
> Cela ne doit être utilisé qu’en tant qu’étape de dépannage. La suppression de cette valeur de chaîne désactive complètement les diffusions SAP dont certains programmes peuvent avoir besoin pour fonctionner correctement.