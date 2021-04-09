---
description: L’application peut demander l’un des deux modes de fonctionnement lors de l’ouverture d’un appareil téléphonique.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Modes de fonctionnement et privilèges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba1cc01ed0552762ac3bc97449b1ae5a923cb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755117"
---
# <a name="operating-modes-and-privileges"></a><span data-ttu-id="38699-103">Modes de fonctionnement et privilèges</span><span class="sxs-lookup"><span data-stu-id="38699-103">Operating Modes and Privileges</span></span>

<span data-ttu-id="38699-104">L’application peut demander l’un des deux modes de fonctionnement lors de l’ouverture d’un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="38699-104">The application can request one of two operating modes when opening a phone device.</span></span> <span data-ttu-id="38699-105">Ces modes reflètent les privilèges que l’application demande pour l’appareil :</span><span class="sxs-lookup"><span data-stu-id="38699-105">These modes reflect the privileges the application requests for the device:</span></span>

-   <span data-ttu-id="38699-106">L’ouverture d’un téléphone pour les privilèges du moniteur permet à l’application de déterminer l’état de l’appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="38699-106">Opening a phone for monitor privileges lets the application determine the status of the phone device.</span></span> <span data-ttu-id="38699-107">Les messages sont envoyés à l’application lorsque des modifications d’État sur l’appareil téléphonique sont détectées.</span><span class="sxs-lookup"><span data-stu-id="38699-107">Messages are sent to the application when status changes on the phone device are detected.</span></span>
-   <span data-ttu-id="38699-108">Une application qui ouvre un appareil téléphonique pour des privilèges de propriétaire peut utiliser des opérations qui modifient l’état du périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="38699-108">An application that opens a phone device for owner privileges can use operations that modify the state of the phone device.</span></span> <span data-ttu-id="38699-109">Le privilège propriétaire comprend également des privilèges d’analyse complets.</span><span class="sxs-lookup"><span data-stu-id="38699-109">Owner privilege automatically includes full monitor privileges as well.</span></span> <span data-ttu-id="38699-110">À tout moment, un appareil téléphonique donné ne peut être ouvert qu’une seule fois pour les privilèges du propriétaire, mais plusieurs fois pour les privilèges du moniteur.</span><span class="sxs-lookup"><span data-stu-id="38699-110">At any time, a given phone device can be open only once for owner privileges, but multiple times for monitor privileges.</span></span> <span data-ttu-id="38699-111">Toutes les opérations **phoneSet** requièrent des privilèges de propriétaire, tandis que toutes les opérations **phoneGet** requièrent uniquement des privilèges d’analyse.</span><span class="sxs-lookup"><span data-stu-id="38699-111">All **phoneSet** operations require owner privileges, while all **phoneGet** operations require only monitor privileges.</span></span>

 

 



