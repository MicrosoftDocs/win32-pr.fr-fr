---
description: En règle générale, un fournisseur fournit des données pour le compte d’une application.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Communication avec votre application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865130"
---
# <a name="communicating-with-your-application"></a><span data-ttu-id="5d3f0-103">Communication avec votre application</span><span class="sxs-lookup"><span data-stu-id="5d3f0-103">Communicating With Your Application</span></span>

<span data-ttu-id="5d3f0-104">En règle générale, un fournisseur fournit des données pour le compte d’une application.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-104">Typically, a provider provides data on behalf of an application.</span></span> <span data-ttu-id="5d3f0-105">Par exemple, un serveur peut créer une DLL de performance pour fournir ses données de compteur.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-105">For example, a server might create a performance DLL to provide its counter data.</span></span> <span data-ttu-id="5d3f0-106">La communication entre une application et son fournisseur diffère pour les applications en mode utilisateur et en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-106">Communication between an application and its provider differs for user-mode and kernel-mode applications.</span></span> <span data-ttu-id="5d3f0-107">Les fournisseurs s’exécutent en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-107">Providers execute in user mode.</span></span> <span data-ttu-id="5d3f0-108">Pour cette raison, les applications en mode utilisateur, telles que les applications d’impression et d’affichage, peuvent utiliser n’importe quelle technique pour la communication entre processus, comme les canaux nommés, le mappage de fichiers ou RPC.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-108">Because of this, user-mode applications, such as print and display applications, can use any technique for interprocess communication, such as named pipes, file mapping, or RPC.</span></span> <span data-ttu-id="5d3f0-109">Toutefois, les applications en mode noyau doivent fournir une interface IOCTL qui retourne les données de performances au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-109">However, kernel-mode applications must provide an IOCTL interface that returns the performance data to the provider.</span></span>

> [!WARNING]
> <span data-ttu-id="5d3f0-110">N’utilisez pas COM comme mécanisme IPC.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-110">Do not use COM as the IPC mechanism.</span></span> <span data-ttu-id="5d3f0-111">Le système ne peut pas garantir l’état d’initialisation COM du thread appelant l’interface.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-111">The system cannot guarantee the COM initialization state of the thread calling the interface.</span></span> <span data-ttu-id="5d3f0-112">Par conséquent, la DLL peut ne pas être en mesure d’initialiser correctement COM et de collecter les données.</span><span class="sxs-lookup"><span data-stu-id="5d3f0-112">Therefore, the DLL may not be able to successfully initialize COM and collect the data.</span></span>

 

 

 



