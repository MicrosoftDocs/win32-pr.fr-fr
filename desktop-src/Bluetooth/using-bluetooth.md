---
title: Utilisation de Bluetooth
description: Cette section décrit les tâches liées à l’écriture d’applications Windows pour Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734532"
---
# <a name="using-bluetooth"></a><span data-ttu-id="5032a-103">Utilisation de Bluetooth</span><span class="sxs-lookup"><span data-stu-id="5032a-103">Using Bluetooth</span></span>

<span data-ttu-id="5032a-104">Cette section décrit les tâches liées à l’écriture d’applications Windows pour Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="5032a-104">This section describes tasks that are related to writing Windows-based applications for Bluetooth.</span></span>

<span data-ttu-id="5032a-105">Bluetooth fournit des définitions de programmation dans les fichiers Ws2bth. h et BluetoothAPIs. h.</span><span class="sxs-lookup"><span data-stu-id="5032a-105">Bluetooth provides programming definitions in the Ws2bth.h and BluetoothAPIs.h files.</span></span> <span data-ttu-id="5032a-106">Le fichier Bthsdpdef. h doit être inclus avant BluetoothAPIs. h.</span><span class="sxs-lookup"><span data-stu-id="5032a-106">The Bthsdpdef.h file must be included before BluetoothAPIs.h.</span></span> <span data-ttu-id="5032a-107">Le fichier Ws2bth. h doit être inclus après Winsock2. h pour utiliser les sockets Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="5032a-107">The Ws2bth.h file must be included after Winsock2.h to use Bluetooth sockets.</span></span> <span data-ttu-id="5032a-108">Liez uniquement à bthprops. lib et évitez la liaison à irprops. lib.</span><span class="sxs-lookup"><span data-stu-id="5032a-108">Link only to Bthprops.lib, and avoid linking to Irprops.lib.</span></span> <span data-ttu-id="5032a-109">Irprops. lib est fourni à des fins de compatibilité descendante uniquement.</span><span class="sxs-lookup"><span data-stu-id="5032a-109">Irprops.lib is provided for backward compatibility only.</span></span> <span data-ttu-id="5032a-110">Bthprops. lib est disponible dans le kit de développement logiciel (SDK) Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5032a-110">Bthprops.lib is available in the Windows Vista SDK.</span></span> <span data-ttu-id="5032a-111">Vous pouvez utiliser le kit de développement logiciel (SDK) Windows Vista pour développer des applications pour Windows XP avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="5032a-111">You can use the Windows Vista SDK to develop applications for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="5032a-112">Le kit de développement logiciel (SDK) Windows Vista est disponible dans le [Centre de téléchargement](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).</span><span class="sxs-lookup"><span data-stu-id="5032a-112">The Windows Vista SDK is available from the [Download Center](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).</span></span>

<span data-ttu-id="5032a-113">Tous les mécanismes standard synchrones et superposés pour lire et écrire des données qui sont actuellement prises en charge avec d’autres familles d’adresses fonctionnent correctement avec la famille d’adresses de la vue \_ BTH.</span><span class="sxs-lookup"><span data-stu-id="5032a-113">All standard synchronous and overlapped mechanisms to read and write data that are currently supported with other address families operate properly with the AF\_BTH address family as well.</span></span>

<span data-ttu-id="5032a-114">Le kit de développement logiciel (SDK) contient un exemple de code qui illustre une application Bluetooth simple utilisant le protocole Winsock 2,2 et RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="5032a-114">There is some example code included with the SDK that shows a simple Bluetooth application using Winsock 2.2 and RFCOMM protocol.</span></span> <span data-ttu-id="5032a-115">Le code source de l’exemple se trouve dans l’emplacement d’installation du kit de développement logiciel (SDK) sous C : \\ Program Files \\ Microsoft SDK \\ Windows \\ <version number> \\ Samples \\ NetDs \\ Winsock \\ Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="5032a-115">The source code for the sample can be found in the SDK installation location under C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\winsock\\Bluetooth.</span></span>

<span data-ttu-id="5032a-116">Cette section décrit les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="5032a-116">This section describes the following topics.</span></span>



| <span data-ttu-id="5032a-117">Section</span><span class="sxs-lookup"><span data-stu-id="5032a-117">Section</span></span>                                                                                      | <span data-ttu-id="5032a-118">Content</span><span class="sxs-lookup"><span data-stu-id="5032a-118">Content</span></span>                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="5032a-119">Programmation Bluetooth avec Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="5032a-119">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md) | <span data-ttu-id="5032a-120">Explique comment utiliser les interfaces Windows Sockets pour implémenter un réseau Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="5032a-120">Explains how to use Windows Sockets interfaces to implement a Bluetooth network.</span></span> |



 

 

 




