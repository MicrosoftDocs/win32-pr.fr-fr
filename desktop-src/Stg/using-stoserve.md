---
title: Utilisation de StoServe
description: StoServe est une DLL destinée principalement à un serveur COM.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513540"
---
# <a name="using-stoserve"></a><span data-ttu-id="614ab-103">Utilisation de StoServe</span><span class="sxs-lookup"><span data-stu-id="614ab-103">Using StoServe</span></span>

<span data-ttu-id="614ab-104">**StoServe** est une dll destinée principalement à un serveur com.</span><span class="sxs-lookup"><span data-stu-id="614ab-104">**StoServe** is a DLL that is intended primarily as a COM server.</span></span> <span data-ttu-id="614ab-105">Bien qu’il puisse être chargé implicitement par liaison à son associé. Fichier LIB, il est normalement utilisé après un appel de LoadLibrary explicite, généralement à partir de la fonction COM [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span><span class="sxs-lookup"><span data-stu-id="614ab-105">Although it can be implicitly loaded by linking to its associated .LIB file, it is normally used after an explicit LoadLibrary call, usually from within the COM function [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span></span> <span data-ttu-id="614ab-106">**StoServe** est un serveur in-process à inscription automatique.</span><span class="sxs-lookup"><span data-stu-id="614ab-106">**StoServe** is a self-registering in-process server.</span></span>

<span data-ttu-id="614ab-107">Pour utiliser **StoServe**, un programme client n’a pas besoin d’inclure StoServe. H ou lien vers STOSERVE. LIB.</span><span class="sxs-lookup"><span data-stu-id="614ab-107">To use **StoServe**, a client program does not need to include STOSERVE.H or link to STOSERVE.LIB.</span></span> <span data-ttu-id="614ab-108">Un client COM de **StoServe** obtient l’accès uniquement via le CLSID de son objet et les services com.</span><span class="sxs-lookup"><span data-stu-id="614ab-108">A COM client of **StoServe** obtains access solely through its object's CLSID and COM services.</span></span> <span data-ttu-id="614ab-109">Pour **StoServe**, le CLSID est CLSID \_ DllPaper (défini dans le fichier PAPGUIDS. H dans le \\ répertoire frère Inc).</span><span class="sxs-lookup"><span data-stu-id="614ab-109">For **StoServe**, that CLSID is CLSID\_DllPaper (defined in file PAPGUIDS.H in the \\INC sibling directory).</span></span> <span data-ttu-id="614ab-110">L’exemple de code [StoClien](structured-storage-client-sample--stoclien-.md) montre comment le client obtient cet accès.</span><span class="sxs-lookup"><span data-stu-id="614ab-110">The [StoClien](structured-storage-client-sample--stoclien-.md) code sample shows how the client obtains this access.</span></span>

<span data-ttu-id="614ab-111">Le Makefile qui génère cet exemple inscrit automatiquement le serveur dans le registre.</span><span class="sxs-lookup"><span data-stu-id="614ab-111">The makefile that builds this sample automatically registers the server in the registry.</span></span> <span data-ttu-id="614ab-112">Vous pouvez lancer manuellement son inscription automatique en émettant la commande suivante à l’invite de commandes dans le répertoire **StoServe** :</span><span class="sxs-lookup"><span data-stu-id="614ab-112">You can manually initiate its self-registration by issuing the following command at the command prompt in the **StoServe** directory:</span></span>

<span data-ttu-id="614ab-113"> **registre** NMAKE</span><span class="sxs-lookup"><span data-stu-id="614ab-113">**nmake** **register**</span></span>

<span data-ttu-id="614ab-114">Cela suppose que vous disposez d’un environnement de compilation configuré.</span><span class="sxs-lookup"><span data-stu-id="614ab-114">This assumes that you have a compilation environment set up.</span></span> <span data-ttu-id="614ab-115">Si ce n’est pas le cas, vous pouvez également appeler directement la commande REGISTER.EXE à l’invite de commandes dans le répertoire **StoServe** .</span><span class="sxs-lookup"><span data-stu-id="614ab-115">If not, you can also directly invoke the REGISTER.EXE command at the command prompt while in the **StoServe** directory.</span></span>

<span data-ttu-id="614ab-116">**..\\ inscrire \\register.exe** **stoserve.dll**</span><span class="sxs-lookup"><span data-stu-id="614ab-116">**..\\register\\register.exe** **stoserve.dll**</span></span>

<span data-ttu-id="614ab-117">Ces commandes d’inscription requièrent une version antérieure de l’exemple REGISTER de cette série, ainsi qu’une version antérieure de STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="614ab-117">These registration commands require a prior build of the REGISTER sample in this series, as well as a prior build of STOSERVE.DLL.</span></span>

<span data-ttu-id="614ab-118">Dans cette série, les Makefiles utilisent l’utilitaire REGISTER.EXE à partir de l’exemple REGISTER.</span><span class="sxs-lookup"><span data-stu-id="614ab-118">In this series, the makefiles use the REGISTER.EXE utility from the REGISTER sample.</span></span> <span data-ttu-id="614ab-119">Les versions récentes du kit de développement logiciel (SDK) de la plateforme et de Visual C++ incluent un utilitaire, REGSVR32.EXE, qui peut être utilisé de la même manière pour inscrire des serveurs in-process et marshaler des dll.</span><span class="sxs-lookup"><span data-stu-id="614ab-119">Recent releases of the Platform Software Development Kit (SDK) and Visual C++ include a utility, REGSVR32.EXE, which can be used in a similar fashion to register in-process servers and marshaling DLLs.</span></span>

<span data-ttu-id="614ab-120">**StoServe** utilise de nombreux services et classes utilitaires fournis par apputil.</span><span class="sxs-lookup"><span data-stu-id="614ab-120">**StoServe** uses many of the utility classes and services provided by APPUTIL.</span></span> <span data-ttu-id="614ab-121">Pour plus d’informations sur APPUTIL, examinez le code source de la bibliothèque APPUTIL dans le répertoire APPUTIL frère et APPUTIL.HTM dans le répertoire principal du didacticiel.</span><span class="sxs-lookup"><span data-stu-id="614ab-121">For more details on APPUTIL, study the APPUTIL library's source code in the sibling APPUTIL directory and APPUTIL.HTM in the main tutorial directory.</span></span>

 

 