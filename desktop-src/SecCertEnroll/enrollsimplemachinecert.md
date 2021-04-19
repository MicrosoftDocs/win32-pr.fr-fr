---
description: Inscrit un ordinateur dans une hiérarchie de certificats à l’aide d’un modèle, d’un nom d’affichage de certificat et de la description du certificat.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: enrollSimpleMachineCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8582bc73fdee7e8be6b2cff8d0aec81b84487307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530580"
---
# <a name="enrollsimplemachinecert"></a><span data-ttu-id="0011f-103">enrollSimpleMachineCert</span><span class="sxs-lookup"><span data-stu-id="0011f-103">enrollSimpleMachineCert</span></span>

<span data-ttu-id="0011f-104">L’exemple enrollSimpleMachineCert inscrit un ordinateur dans une hiérarchie de certificats à l’aide d’un modèle, d’un nom d’affichage de certificat et de la description du certificat.</span><span class="sxs-lookup"><span data-stu-id="0011f-104">The enrollSimpleMachineCert sample enrolls a computer in a certificate hierarchy by using a template, a certificate display name, and the certificate description.</span></span>

## <a name="location"></a><span data-ttu-id="0011f-105">Emplacement</span><span class="sxs-lookup"><span data-stu-id="0011f-105">Location</span></span>

<span data-ttu-id="0011f-106">Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, une version C++ de l’exemple est installée, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ EnrollSimpleMachineCert VC.</span><span class="sxs-lookup"><span data-stu-id="0011f-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\EnrollSimpleMachineCert folder.</span></span> <span data-ttu-id="0011f-107">Une version VBScript est installée dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ EnrollSimpleMachineCert vbs \\ .</span><span class="sxs-lookup"><span data-stu-id="0011f-107">A VBScript version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VBS\\EnrollSimpleMachineCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="0011f-108">Discussions</span><span class="sxs-lookup"><span data-stu-id="0011f-108">Discussion</span></span>

<span data-ttu-id="0011f-109">Exemple enrollSimpleMachineCert :</span><span class="sxs-lookup"><span data-stu-id="0011f-109">The enrollSimpleMachineCert sample:</span></span>

1.  <span data-ttu-id="0011f-110">Traite les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="0011f-110">Processes the command line arguments.</span></span> <span data-ttu-id="0011f-111">La ligne de commande doit contenir le nom du modèle, un nom d’affichage du certificat et une description du certificat.</span><span class="sxs-lookup"><span data-stu-id="0011f-111">The command line should contain the name of the template, a certificate display name, and a certificate description.</span></span>
2.  <span data-ttu-id="0011f-112">Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) et l’initialise à l’aide du modèle spécifié sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="0011f-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template specified on the command line.</span></span> <span data-ttu-id="0011f-113">La valeur ContextAdministratorForceMachine du premier paramètre spécifie que le certificat est demandé par un administrateur agissant pour le compte d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0011f-113">The ContextAdministratorForceMachine value for the first parameter specifies that the certificate is being requested by an administrator acting on behalf of a computer.</span></span>
3.  <span data-ttu-id="0011f-114">Ajoute le nom complet et la description à l’objet d’inscription.</span><span class="sxs-lookup"><span data-stu-id="0011f-114">Adds the display name and description to the enrollment object.</span></span>
4.  <span data-ttu-id="0011f-115">Tente d’inscrire la demande de certificat et vérifie l’état du processus.</span><span class="sxs-lookup"><span data-stu-id="0011f-115">Attempts to enroll the certificate request and checks the status of the process.</span></span> <span data-ttu-id="0011f-116">La fonction checkEnrollStatus est définie dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="0011f-116">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0011f-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0011f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0011f-118">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="0011f-118">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



