---
description: Les auteurs de package peuvent surveiller les messages de Windows Installer internes par le biais de la création d’une application exécutable qui contient un gestionnaire de rappel pour recevoir les messages et les fonctionnalités permettant de lancer une installation.
ms.assetid: 0aa8a2d6-f519-4d87-a28f-a11cb546bff5
title: Surveillance d’une installation à l’aide de MsiSetExternalUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06cc461845a6db1fab4ede22581093c46c0e76e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526260"
---
# <a name="monitoring-an-installation-using-msisetexternalui"></a><span data-ttu-id="0c4b0-103">Surveillance d’une installation à l’aide de MsiSetExternalUI</span><span class="sxs-lookup"><span data-stu-id="0c4b0-103">Monitoring an Installation Using MsiSetExternalUI</span></span>

<span data-ttu-id="0c4b0-104">Les auteurs de package peuvent surveiller les messages de Windows Installer internes par le biais de la création d’une application exécutable qui contient un gestionnaire de rappel pour recevoir les messages et les fonctionnalités permettant de lancer une installation.</span><span class="sxs-lookup"><span data-stu-id="0c4b0-104">Package authors can monitor internal Windows Installer messages through the creation of an executable application that contains both a callback handler to receive the messages and functionality to initiate an installation.</span></span>

<span data-ttu-id="0c4b0-105">Le gestionnaire de rappel est conforme au prototype du \_ Gestionnaire INSTALLUI, et un pointeur vers ce gestionnaire de rappels est passé à [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia).</span><span class="sxs-lookup"><span data-stu-id="0c4b0-105">The callback handler conforms to the INSTALLUI\_HANDLER prototype, and a pointer to this callback handler is passed to [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia).</span></span> <span data-ttu-id="0c4b0-106">Une fois l’installation initiée par un appel à [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), les messages d’installation sont interceptés par le gestionnaire de rappel et l’auteur du package peut afficher ou ignorer de manière sélective tout ou partie de ces messages.</span><span class="sxs-lookup"><span data-stu-id="0c4b0-106">Once the installation has been initiated by a call to [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), installation messages are trapped by the callback handler and the package author can selectively display or ignore any or all of these messages.</span></span>

<span data-ttu-id="0c4b0-107">Pour plus d’informations, consultez [gestion des messages de progression à l’aide de MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), [retour de valeurs à partir d’un gestionnaire d’interface utilisateur externe](returning-values-from-an-external-user-interface-handler.md)et [analyse des messages de Windows Installer](parsing-windows-installer-messages.md).</span><span class="sxs-lookup"><span data-stu-id="0c4b0-107">For more information, see [Handling Progress Messages Using MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), [Returning Values from an External User Interface Handler](returning-values-from-an-external-user-interface-handler.md), and [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="0c4b0-108">Pour plus d’informations sur l’utilisation d’un gestionnaire externe basé sur les enregistrements, consultez [surveillance d’une installation à l’aide de MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).</span><span class="sxs-lookup"><span data-stu-id="0c4b0-108">For more information about using a record-based external handler, see [Monitoring an Installation Using MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).</span></span>

 

 



