---
description: Utilisez CertMgr pour afficher des certificats, des listes de révocation de certificats et des listes CTL à partir d’un fichier ou d’un magasin de certificats, copier des certificats dans un magasin de certificats, supprimer des certificats d’un magasin de certificats et enregistrer des certificats dans des fichiers.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Utilisation de CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527200"
---
# <a name="using-certmgr"></a><span data-ttu-id="00b32-103">Utilisation de CertMgr</span><span class="sxs-lookup"><span data-stu-id="00b32-103">Using CertMgr</span></span>

<span data-ttu-id="00b32-104">Vous pouvez utiliser [certmgr](certmgr.md) [*pour afficher des certificats,*](../secgloss/c-gly.md)des [*listes de révocation*](../secgloss/c-gly.md) de certificats (CRL) et des listes de certificats de [*confiance*](../secgloss/c-gly.md) (CTL) à partir d’un fichier ou d’un magasin de certificats, copier des certificats dans un [*magasin de certificats*](../secgloss/c-gly.md), supprimer des certificats d’un magasin de certificats et enregistrer des certificats dans des fichiers.</span><span class="sxs-lookup"><span data-stu-id="00b32-104">[CertMgr](certmgr.md) can be used to view [*certificates*](../secgloss/c-gly.md), [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) from a file or a certificate store, to copy certificates into a [*certificate store*](../secgloss/c-gly.md), to delete certificates from a certificate store, and to save certificates to files.</span></span>

<span data-ttu-id="00b32-105">Lorsque [certmgr](certmgr.md) est utilisé sans options, un Assistant certmgr s’affiche pour guider l’utilisateur tout au long de l’opération.</span><span class="sxs-lookup"><span data-stu-id="00b32-105">When [CertMgr](certmgr.md) is used without options, a CertMgr wizard appears to guide the user through the operation.</span></span>

<span data-ttu-id="00b32-106">Le fichier doit être de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="00b32-106">The file must be one of the following types:</span></span>

-   <span data-ttu-id="00b32-107">Un fichier de certificat, de liste de révocation de certificats ou de liste de révocation de certificats encodé (peut être encodé en base 64)</span><span class="sxs-lookup"><span data-stu-id="00b32-107">An encoded CTL, CRL, or certificate file (could be base-64 encoded)</span></span>
-   <span data-ttu-id="00b32-108">Un \# fichier PKCS 7</span><span class="sxs-lookup"><span data-stu-id="00b32-108">A PKCS \#7 file</span></span>
-   <span data-ttu-id="00b32-109">Un fichier SPC</span><span class="sxs-lookup"><span data-stu-id="00b32-109">An SPC file</span></span>
-   <span data-ttu-id="00b32-110">Un document signé</span><span class="sxs-lookup"><span data-stu-id="00b32-110">A signed document</span></span>
-   <span data-ttu-id="00b32-111">StoreFile sérialisé</span><span class="sxs-lookup"><span data-stu-id="00b32-111">A serialized storeFile</span></span>

<span data-ttu-id="00b32-112">Les exemples suivants utilisent des commandes [certmgr](certmgr.md) pour effectuer des tâches de certificat courantes.</span><span class="sxs-lookup"><span data-stu-id="00b32-112">The following examples use [CertMgr](certmgr.md) commands to perform common certificate tasks.</span></span>

-   <span data-ttu-id="00b32-113">Affichez les certificats, les listes de révocation de certificats et les listes CTL de *MyFile. ext*.</span><span class="sxs-lookup"><span data-stu-id="00b32-113">View the certificates, CRLs, and CTLs from *MyFile.ext*.</span></span>

    <span data-ttu-id="00b32-114">**certmgr** *MyFile. ext*</span><span class="sxs-lookup"><span data-stu-id="00b32-114">**certmgr** *MyFile.ext*</span></span>

-   <span data-ttu-id="00b32-115">Affichez les certificats, les listes de révocation de certificats et les listes CTL à partir du magasin mon système.</span><span class="sxs-lookup"><span data-stu-id="00b32-115">View the certificates, CRLs, and CTLs from the MY system store.</span></span>

    <span data-ttu-id="00b32-116">**certmgr-s My**</span><span class="sxs-lookup"><span data-stu-id="00b32-116">**certmgr -s my**</span></span>

-   <span data-ttu-id="00b32-117">Copiez tous les certificats, listes de révocation de certificats et listes de certificats de confiance dans un fichier nommé *MyFile. ext* dans un nouveau fichier nommé *NewFile. ext*.</span><span class="sxs-lookup"><span data-stu-id="00b32-117">Copy all the certificates, CRLs, and CTLs in a file named *MyFile.ext* to a new file, called *NewFile.ext*.</span></span>

    <span data-ttu-id="00b32-118">**certmgr-Add-All-c** *MyFile. ext* *NewFile. ext*</span><span class="sxs-lookup"><span data-stu-id="00b32-118">**certmgr -add -all -c** *MyFile.ext* *NewFile.ext*</span></span>

-   <span data-ttu-id="00b32-119">Copiez tous les certificats, listes de révocation de certificats et listes de certificats de confiance du magasin MY System dans un fichier appelé *NewMyFile. ext*.</span><span class="sxs-lookup"><span data-stu-id="00b32-119">Copy all the certificates, CRLs, and CTLs from the MY system store to a file called *NewMyFile.ext*.</span></span>

    <span data-ttu-id="00b32-120">**certmgr-Add-All-c-s My** *NewMyFile. ext*</span><span class="sxs-lookup"><span data-stu-id="00b32-120">**certmgr -add -all -c -s my** *NewMyFile.ext*</span></span>

-   <span data-ttu-id="00b32-121">Copiez un certificat avec le nom commun *myCert* dans le magasin My System dans un fichier appelé *newCert. cer*.</span><span class="sxs-lookup"><span data-stu-id="00b32-121">Copy a certificate with the common name *MyCert* in the MY system store to a file called *NewCert.cer*.</span></span>

    <span data-ttu-id="00b32-122">**certmgr-Add-c-n** *myCert* **-s My** *newCert. cer*</span><span class="sxs-lookup"><span data-stu-id="00b32-122">**certmgr -add -c -n** *MyCert* **-s my** *NewCert.cer*</span></span>

-   <span data-ttu-id="00b32-123">Supprimez tous les certificats du magasin mon système.</span><span class="sxs-lookup"><span data-stu-id="00b32-123">Delete all the certificates from the MY system store.</span></span>

    <span data-ttu-id="00b32-124">**certmgr-del-All-c-s My**</span><span class="sxs-lookup"><span data-stu-id="00b32-124">**certmgr -del -all -c -s my**</span></span>

-   <span data-ttu-id="00b32-125">Supprimez toutes les listes CTL du magasin MY System et enregistrez le magasin qui en résulte dans un fichier appelé *NewStore. Str*.</span><span class="sxs-lookup"><span data-stu-id="00b32-125">Delete all the CTLs from the MY system store and save the resulting store to a file called *NewStore.str*.</span></span>

    <span data-ttu-id="00b32-126">**certmgr-del-All-CTL-s My** *NewStore. Str*</span><span class="sxs-lookup"><span data-stu-id="00b32-126">**certmgr -del -all -ctl -s my** *NewStore.str*</span></span>

-   <span data-ttu-id="00b32-127">Enregistrez dans un fichier nommé *newCert. cer*, un certificat qui est un certificat encodé [*X. 509*](../secgloss/x-gly.md) , dont le nom commun est *myCert*, et qui se trouve dans le magasin de certificats racine.</span><span class="sxs-lookup"><span data-stu-id="00b32-127">Save, to a file called *NewCert.cer*, a certificate that is an [*X.509*](../secgloss/x-gly.md) encoded certificate, that has the common name *MyCert*, and that is located in the Root certificate store.</span></span>

    <span data-ttu-id="00b32-128">**certmgr-put-c-n** *myCert* **-s racine** *newCert. cer*</span><span class="sxs-lookup"><span data-stu-id="00b32-128">**certmgr -put -c -n** *MyCert* **-s root** *NewCert.cer*</span></span>

## <a name="related-topics"></a><span data-ttu-id="00b32-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="00b32-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00b32-130">CertMgr</span><span class="sxs-lookup"><span data-stu-id="00b32-130">CertMgr</span></span>](certmgr.md)
</dt> </dl>

 

 
