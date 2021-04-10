---
description: La fonction DeviceIoControl fournit une interface de contrôle d’entrée et de sortie de l’appareil (IOCTL) par le biais de laquelle une application peut communiquer directement avec un pilote de périphérique.
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: Contrôle d’entrée et de sortie de l’appareil (IOCTL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2bb2ee26c63c2aad02d8e8d167ff12383fc6b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861486"
---
# <a name="device-input-and-output-control-ioctl"></a><span data-ttu-id="20288-103">Contrôle d’entrée et de sortie de l’appareil (IOCTL)</span><span class="sxs-lookup"><span data-stu-id="20288-103">Device Input and Output Control (IOCTL)</span></span>

<span data-ttu-id="20288-104">La fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) fournit une interface de contrôle d’entrée et de sortie de l’appareil (IOCTL) par le biais de laquelle une application peut communiquer directement avec un pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="20288-104">The [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function provides a device input and output control (IOCTL) interface through which an application can communicate directly with a device driver.</span></span> <span data-ttu-id="20288-105">La fonction **DeviceIoControl** est une interface à usage général qui peut envoyer des codes de contrôle à un large éventail d’appareils.</span><span class="sxs-lookup"><span data-stu-id="20288-105">The **DeviceIoControl** function is a general-purpose interface that can send control codes to a variety of devices.</span></span> <span data-ttu-id="20288-106">Chaque code de contrôle représente une opération que le pilote doit effectuer.</span><span class="sxs-lookup"><span data-stu-id="20288-106">Each control code represents an operation for the driver to perform.</span></span> <span data-ttu-id="20288-107">Par exemple, un code de contrôle peut demander à un pilote de périphérique de retourner des informations sur l’appareil correspondant ou indiquer au pilote d’effectuer une action sur l’appareil, comme la mise en forme d’un disque.</span><span class="sxs-lookup"><span data-stu-id="20288-107">For example, a control code can ask a device driver to return information about the corresponding device, or direct the driver to carry out an action on the device, such as formatting a disk.</span></span>

<span data-ttu-id="20288-108">Un certain nombre de codes de contrôle standard sont définis dans les fichiers d’en-tête du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="20288-108">A number of standard control codes are defined in the SDK header files.</span></span> <span data-ttu-id="20288-109">En outre, les pilotes de périphérique peuvent définir leurs propres codes de contrôle spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="20288-109">In addition, device drivers can define their own device-specific control codes.</span></span> <span data-ttu-id="20288-110">Pour obtenir la liste des codes de contrôle standard inclus dans la documentation du kit de développement logiciel (SDK), consultez la section Notes de [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span><span class="sxs-lookup"><span data-stu-id="20288-110">For a list of standard control codes included in the SDK documentation, see the Remarks section of [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span></span>

<span data-ttu-id="20288-111">Les types de codes de contrôle que vous pouvez spécifier dépendent de l’appareil accédé et de la plateforme sur laquelle votre application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="20288-111">The types of control codes you can specify depend on the device being accessed and the platform on which your application is running.</span></span> <span data-ttu-id="20288-112">Les applications peuvent utiliser les codes de contrôle standard ou les codes de contrôle spécifiques à l’appareil pour effectuer des opérations d’entrée et de sortie directes sur un lecteur de disquette, un lecteur de disque dur, un lecteur de bande ou un lecteur de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="20288-112">Applications can use the standard control codes or device-specific control codes to perform direct input and output operations on a floppy disk drive, hard disk drive, tape drive, or CD-ROM drive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20288-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20288-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20288-114">Appeler DeviceIoControl</span><span class="sxs-lookup"><span data-stu-id="20288-114">Calling DeviceIoControl</span></span>](calling-deviceiocontrol.md)
</dt> </dl>

 

 
