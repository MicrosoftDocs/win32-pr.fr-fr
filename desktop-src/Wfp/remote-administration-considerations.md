---
description: Certaines considérations sont spécifiques aux systèmes administrés à distance.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Considérations relatives à l’administration à distance WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bb40776f6b727abb49d7e0685bb12b087ed2bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530152"
---
# <a name="wfp-remote-administration-considerations"></a><span data-ttu-id="abff0-103">Considérations relatives à l’administration à distance WFP</span><span class="sxs-lookup"><span data-stu-id="abff0-103">WFP Remote Administration Considerations</span></span>

<span data-ttu-id="abff0-104">Certaines considérations sont spécifiques aux systèmes administrés à distance.</span><span class="sxs-lookup"><span data-stu-id="abff0-104">There are some considerations that are unique to remotely administered systems.</span></span> <span data-ttu-id="abff0-105">Tout d’abord, lorsque l’installation du logiciel est déployée à distance (à l’aide de SMS ou de MSI), des boîtes de dialogue d’erreur WFP s’affichent à l’écran d’un administrateur connecté localement (le cas échéant), et non au service d’installation.</span><span class="sxs-lookup"><span data-stu-id="abff0-105">First, when software installation is remotely deployed (using SMS or MSI), WFP error dialog boxes are displayed on the screen of a locally logged on administrator (if present), not to the installation service.</span></span> <span data-ttu-id="abff0-106">Deuxièmement, si un administrateur se connecte à un serveur Terminal Server à distance et installe une application qui remplace les fichiers système protégés, les boîtes de dialogue d’erreur WFP s’affichent uniquement dans la console principale, et non dans la fenêtre distante de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="abff0-106">Second, if an administrator logs into a terminal server remotely and installs an application that replaces protected system files, the WFP error dialog boxes are displayed only in the main console, not the administrator's remote window.</span></span>

<span data-ttu-id="abff0-107">Pour ces raisons, WFP supprime ses boîtes de dialogue d’erreur jusqu’à ce qu’un administrateur se connecte localement.</span><span class="sxs-lookup"><span data-stu-id="abff0-107">For these reasons, WFP suppresses its error dialog boxes until an administrator logs on locally.</span></span> <span data-ttu-id="abff0-108">Les administrateurs distants peuvent trouver des erreurs de remplacement de fichier dans le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="abff0-108">Remote administrators can find file replacement errors in the system event log.</span></span>

<span data-ttu-id="abff0-109">**Windows Vista et Windows Server 2008 :** L’administration à distance de WFP n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="abff0-109">**Windows Vista and Windows Server 2008:** WFP remote administration is not supported.</span></span>

 

 



