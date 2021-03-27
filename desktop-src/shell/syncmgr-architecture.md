---
description: Le gestionnaire de synchronisation comprend des composants de l’interface utilisateur, tels que les boîtes de dialogue à onglets du service SyncMgr, des boîtes de dialogue d’erreur et des boîtes de dialogue de progression.
title: Architecture du gestionnaire de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f178b407c1f7d568c9de2ce7c81d937e7d1cdef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760509"
---
# <a name="synchronization-manager-architecture"></a><span data-ttu-id="374d4-103">Architecture du gestionnaire de synchronisation</span><span class="sxs-lookup"><span data-stu-id="374d4-103">Synchronization Manager Architecture</span></span>

<span data-ttu-id="374d4-104">Le gestionnaire de synchronisation comprend des composants de l’interface utilisateur, tels que les boîtes de dialogue à onglets du service SyncMgr, des boîtes de dialogue d’erreur et des boîtes de dialogue de progression.</span><span class="sxs-lookup"><span data-stu-id="374d4-104">The Synchronization Manager includes user interface components, such as the tabbed dialog boxes in the SyncMgr service, error dialogs, and progress dialogs.</span></span> <span data-ttu-id="374d4-105">Avec les composants de l’interface utilisateur, l’utilisateur final peut planifier des applications pour la synchronisation et configurer la synchronisation automatique pour qu’elle se produise conjointement avec les événements système spécifiés.</span><span class="sxs-lookup"><span data-stu-id="374d4-105">With the user interface components the end user can schedule applications for synchronization and set up automatic synchronization to occur in conjunction with specified system events.</span></span> <span data-ttu-id="374d4-106">Par exemple, le SyncMgr peut être appelé lors de l’ouverture de session de l’utilisateur ou de l’arrêt du système.</span><span class="sxs-lookup"><span data-stu-id="374d4-106">For example, the SyncMgr can be invoked at user logon or system shutdown.</span></span> <span data-ttu-id="374d4-107">L’utilisateur peut également appeler une synchronisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="374d4-107">The user can also invoke a manual synchronization.</span></span>

<span data-ttu-id="374d4-108">L’utilisateur sélectionne une application et spécifie les éléments de l’application à synchroniser et définit un événement déclencheur.</span><span class="sxs-lookup"><span data-stu-id="374d4-108">The user selects an application and specifies the items within the application to be synchronized and sets a trigger event.</span></span> <span data-ttu-id="374d4-109">Par exemple, dans une application de messagerie, la boîte de réception, la boîte d’envoi ou un autre dossier contenant des messages peut être un élément distinct pour l’application.</span><span class="sxs-lookup"><span data-stu-id="374d4-109">For example, within an email application, the Inbox, the Outbox, or some other folder containing messages can be a separate item for the application.</span></span>

<span data-ttu-id="374d4-110">SyncMgr comprend également une interface de programmation qui permet aux applications de s’inscrire pour utiliser les fonctionnalités de synchronisation, de traiter les erreurs et de recevoir des informations de progression et des notifications pendant le processus de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="374d4-110">SyncMgr also includes a programming interface so that applications can register to use synchronization features, can process errors, and can receive progress information and notifications during the synchronization process.</span></span>

 

 



