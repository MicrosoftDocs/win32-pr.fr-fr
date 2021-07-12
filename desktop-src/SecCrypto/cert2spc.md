---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581977"
---
# <a name="cert2spc"></a><span data-ttu-id="90344-103">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="90344-103">Cert2SPC</span></span>

<span data-ttu-id="90344-104">l’outil Cert2SPC crée un certificat SPC (test [*Software Publisher certificate*](../secgloss/s-gly.md) ) à l’aide de [*certificats*](../secgloss/c-gly.md) [*X. 509*](../secgloss/x-gly.md) existants.</span><span class="sxs-lookup"><span data-stu-id="90344-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="90344-105">Cert2SPC peut encapsuler plusieurs certificats X. 509 dans un objet de données signées [*PKCS \# 7*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="90344-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="90344-106">l’outil est installé dans le \\ dossier Bin du chemin d’installation du kit de développement logiciel (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="90344-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="90344-107">Cert2SPC est disponible dans le cadre de la SDK Windows, que vous pouvez télécharger à partir de <https://go.microsoft.com/fwlink/p/?linkid=84091> .</span><span class="sxs-lookup"><span data-stu-id="90344-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="90344-108">Cet outil est destiné à des fins de test uniquement.</span><span class="sxs-lookup"><span data-stu-id="90344-108">This tool is for test purposes only.</span></span> <span data-ttu-id="90344-109">Un SPC valide est obtenu à partir d’une [*autorité de certification*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="90344-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="90344-110">**Cert2spc** *Cert1. cer Cert2. cer* ...</span><span class="sxs-lookup"><span data-stu-id="90344-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="90344-111">*Sortie. spc*</span><span class="sxs-lookup"><span data-stu-id="90344-111">*Output.spc*</span></span>

 



| <span data-ttu-id="90344-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90344-112">Parameters</span></span>              | <span data-ttu-id="90344-113">Description</span><span class="sxs-lookup"><span data-stu-id="90344-113">Description</span></span>                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90344-114">*Cert1. cer Cert2. cer* ...</span><span class="sxs-lookup"><span data-stu-id="90344-114">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="90344-115">Noms des certificats X. 509 à inclure dans le SPC.</span><span class="sxs-lookup"><span data-stu-id="90344-115">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="90344-116">Chaque nom de certificat se termine par l’extension. cer.</span><span class="sxs-lookup"><span data-stu-id="90344-116">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="90344-117">*Sortie. spc*</span><span class="sxs-lookup"><span data-stu-id="90344-117">*Output.spc*</span></span>            | <span data-ttu-id="90344-118">Nom de l' \# objet PKCS 7 qui contient les certificats X. 509 à créer.</span><span class="sxs-lookup"><span data-stu-id="90344-118">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="90344-119">Le nom du fichier de sortie se termine par l’extension. spc.</span><span class="sxs-lookup"><span data-stu-id="90344-119">The output file name ends with the .spc extension.</span></span> |



 

 

 
