---
description: Avant que le moteur de configuration de la sécurité puisse appeler votre moteur d’attachement pour traiter des tâches spécifiques au service, vous devez installer votre moteur de pièces jointes et l’inscrire auprès du moteur de configuration de sécurité.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Inscription d’un moteur de pièce jointe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514162"
---
# <a name="registering-an-attachment-engine"></a><span data-ttu-id="65361-103">Inscription d’un moteur de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="65361-103">Registering an Attachment Engine</span></span>

<span data-ttu-id="65361-104">Avant que le moteur de configuration de la sécurité puisse appeler votre moteur d’attachement pour traiter des tâches spécifiques au service, vous devez installer votre moteur de pièces jointes et l’inscrire auprès du moteur de configuration de sécurité.</span><span class="sxs-lookup"><span data-stu-id="65361-104">Before the Security Configuration Engine can call your attachment engine to process service-specific tasks, you must install your attachment engine and register it with the Security Configuration Engine.</span></span>

<span data-ttu-id="65361-105">**Pour installer et inscrire la DLL du moteur de pièces jointes**</span><span class="sxs-lookup"><span data-stu-id="65361-105">**To install and register the attachment engine DLL**</span></span>

1.  <span data-ttu-id="65361-106">Copiez la DLL du moteur de pièces jointes dans un répertoire sur le système.</span><span class="sxs-lookup"><span data-stu-id="65361-106">Copy the attachment engine DLL to a directory on the system.</span></span> <span data-ttu-id="65361-107">Le répertoire préféré est% windir% \\ secedit \\ Attachments.</span><span class="sxs-lookup"><span data-stu-id="65361-107">The preferred directory is %windir%\\secedit\\attachments.</span></span> <span data-ttu-id="65361-108">Si ce répertoire n’existe pas, vous devez le créer.</span><span class="sxs-lookup"><span data-stu-id="65361-108">If this directory does not exist, you should create it.</span></span>
2.  <span data-ttu-id="65361-109">Créez une clé de Registre sous le nœud suivant.</span><span class="sxs-lookup"><span data-stu-id="65361-109">Create a registry key under the following node.</span></span> <span data-ttu-id="65361-110">Le nom du *service* est le nom inscrit pour la pièce jointe et doit être le même nom de service que celui utilisé dans le gestionnaire de contrôle des services, un module qui gère l’arrêt et le démarrage des services.</span><span class="sxs-lookup"><span data-stu-id="65361-110">The *service name* is the registered name for the attachment, and must be the same service name used in the Service Control Manager, a module which manages the stopping and starting of services.</span></span> <span data-ttu-id="65361-111">Le nom doit également être unique, de sorte qu’il n’est pas en conflit avec les noms des autres pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="65361-111">The name must also be unique so it does not conflict with the names of other attachments.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  <span data-ttu-id="65361-112">Créez la valeur de chaîne suivante dans la nouvelle clé de registre.</span><span class="sxs-lookup"><span data-stu-id="65361-112">Create the following string value in the new registry key.</span></span> <span data-ttu-id="65361-113">le *chemin d’accès du moteur des pièces jointes* est le chemin d’accès complet au module du moteur d’attachement.</span><span class="sxs-lookup"><span data-stu-id="65361-113">*attachment engine path* is the full path to the attachment engine module.</span></span><dl> <dd><span data-ttu-id="65361-114">**ServiceAttachmentPath**  =  *chemin du moteur des pièces jointes*</span><span class="sxs-lookup"><span data-stu-id="65361-114">**ServiceAttachmentPath** = *attachment engine path*</span></span><dl> <dt>

<span data-ttu-id="65361-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="65361-115">Data type</span></span>
</dt> <dd><span data-ttu-id="65361-116">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="65361-116">REG_SZ</span></span></dd> </dl> </dd> </dl>

 

 



