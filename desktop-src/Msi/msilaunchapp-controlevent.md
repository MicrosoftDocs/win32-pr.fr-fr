---
description: Cet événement de contrôle exécute un fichier spécifié. Si le fichier n’existe pas ou si l’événement échoue, Windows Installer journalise l’erreur dans le journal détaillé sans afficher de boîte de dialogue contenant un message d’erreur.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521470"
---
# <a name="msilaunchapp-controlevent"></a><span data-ttu-id="d6325-104">MsiLaunchApp ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d6325-104">MsiLaunchApp ControlEvent</span></span>

<span data-ttu-id="d6325-105">Cet événement de contrôle exécute un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="d6325-105">This control event runs a specified file.</span></span> <span data-ttu-id="d6325-106">Si le fichier n’existe pas ou si l’événement échoue, Windows Installer journalise l’erreur dans le journal détaillé sans afficher de boîte de dialogue contenant un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d6325-106">If the file does not exist, or if the event fails, Windows Installer logs the error in the verbose log without displaying a dialog box containing an error message.</span></span>

<span data-ttu-id="d6325-107">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d6325-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="d6325-108">Ce ControlEvent, est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="d6325-108">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

## <a name="published-by"></a><span data-ttu-id="d6325-109">Publié par</span><span class="sxs-lookup"><span data-stu-id="d6325-109">Published By</span></span>

<span data-ttu-id="d6325-110">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="d6325-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="d6325-111">Argument</span><span class="sxs-lookup"><span data-stu-id="d6325-111">Argument</span></span>

<span data-ttu-id="d6325-112">Les champs de la valeur de l’argument sont délimités par des espaces.</span><span class="sxs-lookup"><span data-stu-id="d6325-112">The fields of the argument value are delimited by spaces.</span></span> <span data-ttu-id="d6325-113">Le premier champ contient une valeur de chaîne qui spécifie le fichier à exécuter.</span><span class="sxs-lookup"><span data-stu-id="d6325-113">The first field contains a string value that specifies the file that is to be run.</span></span> <span data-ttu-id="d6325-114">Utilisez la valeur de chaîne \[ \# *filekey* \] pour identifier le fichier et remplacer *filekey* par l’identificateur du fichier figurant dans la colonne fichier de la table de [fichiers](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d6325-114">Use a string value of \[\#*filekey*\] to identify the file and replace *filekey* with the file's identifier appearing in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="d6325-115">Les champs restants de l’argument peuvent contenir des paramètres utilisés par le fichier en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d6325-115">Any remaining fields of the argument can contain parameters being used by the file being run.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="d6325-116">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="d6325-116">Action on Subscribers</span></span>

<span data-ttu-id="d6325-117">Ce ControlEvent, n’effectue aucune action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="d6325-117">This ControlEvent performs no actions on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="d6325-118">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="d6325-118">Typical Use</span></span>

<span data-ttu-id="d6325-119">Pour permettre à un utilisateur de choisir d’exécuter un fichier à la fin d’une installation.</span><span class="sxs-lookup"><span data-stu-id="d6325-119">To enable a user to choose to run a file at the end of an installation.</span></span> <span data-ttu-id="d6325-120">Cet événement peut être conditionné sur une propriété définie par un contrôle de [case à cocher](checkbox-control.md) affiché dans la dernière boîte de dialogue de l’installation.</span><span class="sxs-lookup"><span data-stu-id="d6325-120">This event can be conditioned on a property set by a [CheckBox](checkbox-control.md) control displayed on the final dialog box of the installation.</span></span> <span data-ttu-id="d6325-121">Le contrôle de case à cocher ne doit pas être affiché pendant la suppression du package.</span><span class="sxs-lookup"><span data-stu-id="d6325-121">The CheckBox control should not be displayed during the removal of the package.</span></span>

 

 



