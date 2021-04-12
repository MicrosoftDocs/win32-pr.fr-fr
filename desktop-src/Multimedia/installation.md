---
title: Installation (Windows Multimedia)
description: Installation
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- pilotes installables, installation
- pilotes installables, DRV_INSTALL message
- pilotes installables, DRV_REMOVE message
- Message DRV_INSTALL
- Message DRV_REMOVE
- Message DRVCONFIGINFO
- installation des pilotes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ebebd090c7499698c59c325d1ac0d487902454
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383632"
---
# <a name="installation-windows-multimedia"></a><span data-ttu-id="eaf0d-110">Installation (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="eaf0d-110">Installation (Windows Multimedia)</span></span>

<span data-ttu-id="eaf0d-111">Un pilote pouvant être installé peut effectuer des tâches d’installation spécifiques au pilote lors du traitement des messages de [**\_ suppression**](drv-remove.md) de [**DRV \_ install**](drv-install.md) et DRV.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-111">An installable driver can carry out driver-specific installation tasks when processing the [**DRV\_INSTALL**](drv-install.md) and [**DRV\_REMOVE**](drv-remove.md) messages.</span></span> <span data-ttu-id="eaf0d-112">Une application d’installation, telle qu’une application de panneau de configuration, envoie les messages au pilote lors de l’installation ou de la suppression du pilote, respectivement.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-112">An installation application, such as a Control Panel application, sends the messages to the driver when installing or removing the driver, respectively.</span></span>

<span data-ttu-id="eaf0d-113">Lors du traitement du \_ message d’installation de DRV, le pilote vérifie généralement que le matériel requis est présent, puis affiche la boîte de dialogue de configuration pour permettre à l’utilisateur de choisir les paramètres de configuration initiaux pour le pilote et le matériel associé.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-113">When processing the DRV\_INSTALL message, the driver typically verifies that the required hardware is present and then displays the configuration dialog box to let the user choose the initial configuration settings for the driver and associated hardware.</span></span> <span data-ttu-id="eaf0d-114">Le message inclut l’adresse d’une structure [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) qui contient les noms de la clé de Registre et la valeur associée au pilote. le pilote vérifie la valeur de Registre pour les informations de configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-114">The message includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver; the driver checks the registry value for default configuration information.</span></span> <span data-ttu-id="eaf0d-115">Enfin, le pilote crée également des clés de Registre et des valeurs supplémentaires nécessaires pour réussir l’opération.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-115">Finally, the driver also creates any additional registry keys and values needed for successful operation.</span></span>

<span data-ttu-id="eaf0d-116">Lors du traitement du \_ message de suppression du DRV, le pilote supprime toutes les clés de Registre et les valeurs que vous avez créées.</span><span class="sxs-lookup"><span data-stu-id="eaf0d-116">When processing the DRV\_REMOVE message, the driver removes any registry keys and values it may have created.</span></span>

 

 
