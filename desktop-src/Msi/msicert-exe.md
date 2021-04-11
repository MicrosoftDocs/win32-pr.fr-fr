---
description: Windows Installer pouvez utiliser des signatures numériques pour détecter les ressources endommagées.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4df800bbcfa9ed2fb0d016794b3ebcf1535be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210782"
---
# <a name="msicertexe"></a><span data-ttu-id="9c9a4-103">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="9c9a4-103">Msicert.exe</span></span>

<span data-ttu-id="9c9a4-104">Windows Installer pouvez utiliser des signatures numériques pour détecter les ressources endommagées.</span><span class="sxs-lookup"><span data-stu-id="9c9a4-104">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="9c9a4-105">Un certificat de signataire peut être comparé au certificat de signataire d’une ressource externe qui doit être installée par le package.</span><span class="sxs-lookup"><span data-stu-id="9c9a4-105">A signer certificate may be compared to the signer certificate of an external resource to be installed by the package.</span></span> <span data-ttu-id="9c9a4-106">Pour plus d’informations, consultez [signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="9c9a4-106">For more information, see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="9c9a4-107">MsiCert.exe est un utilitaire de ligne de commande qui peut être utilisé pour remplir la table [MsiDigitalSignature](msidigitalsignature-table.md) et la [table MsiDigitalCertificate](msidigitalcertificate-table.md) avec les informations de signature numérique d’un fichier CAB externe.</span><span class="sxs-lookup"><span data-stu-id="9c9a4-107">MsiCert.exe is a command line utility that can be used to populate the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md) with the digital signature information of an external cabinet file.</span></span> <span data-ttu-id="9c9a4-108">Le fichier cab doit être signé numériquement et listé dans la [table des médias](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="9c9a4-108">The cabinet file must by digitally signed and listed in the [Media table](media-table.md).</span></span> <span data-ttu-id="9c9a4-109">MsiCert.exe utilise les informations de certificat du signataire de l’armoire signée numériquement et crée et ajoute les tables MsiDigitalSignature et MsiDigitalCertificate à la base de données si elles n’existent pas déjà.</span><span class="sxs-lookup"><span data-stu-id="9c9a4-109">MsiCert.exe uses the signer certificate information from the digitally signed cabinet and will create and add the MsiDigitalSignature and MsiDigitalCertificate tables to the database if they do not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c9a4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c9a4-110">Syntax</span></span>

<span data-ttu-id="9c9a4-111">**msicert-d** *{base de données}* **-m** *{entrée de support}* **-c** *{Cabinet}* **\[ -h \]**</span><span class="sxs-lookup"><span data-stu-id="9c9a4-111">**msicert -d** *{database}* **-m** *{media entry}* **-c** *{cabinet}* **\[-h\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="9c9a4-112">Options de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="9c9a4-112">Command Line Options</span></span>

<span data-ttu-id="9c9a4-113">Les options de ligne de commande ne respectent pas la casse et les séparateurs de barres obliques peuvent être utilisés à la place d’un tiret.</span><span class="sxs-lookup"><span data-stu-id="9c9a4-113">The command line options are case-insensitive and slash delimiters may be used instead of a dash.</span></span>



| <span data-ttu-id="9c9a4-114">Option</span><span class="sxs-lookup"><span data-stu-id="9c9a4-114">Option</span></span> | <span data-ttu-id="9c9a4-115">Paramètre</span><span class="sxs-lookup"><span data-stu-id="9c9a4-115">Parameter</span></span>        | <span data-ttu-id="9c9a4-116">Description</span><span class="sxs-lookup"><span data-stu-id="9c9a4-116">Description</span></span>                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9a4-117">-d</span><span class="sxs-lookup"><span data-stu-id="9c9a4-117">-d</span></span>     | <database> | <span data-ttu-id="9c9a4-118">La base de données (fichier. msi) qui est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="9c9a4-118">The database (.msi file) that is being updated.</span></span>                                                         |
| <span data-ttu-id="9c9a4-119">-M</span><span class="sxs-lookup"><span data-stu-id="9c9a4-119">-m</span></span>     | <media Id> | <span data-ttu-id="9c9a4-120">Entrée dans le champ depatinage de la [table Media](media-table.md) de l’enregistrement du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="9c9a4-120">The entry in the DiskId field of the [Media table](media-table.md) in the record for the cabinet file.</span></span> |
| <span data-ttu-id="9c9a4-121">-c</span><span class="sxs-lookup"><span data-stu-id="9c9a4-121">-c</span></span>     | <cabinet>  | <span data-ttu-id="9c9a4-122">Chemin d’accès au fichier CAB signé numériquement.</span><span class="sxs-lookup"><span data-stu-id="9c9a4-122">The path to the digitally signed cabinet file.</span></span>                                                          |
| <span data-ttu-id="9c9a4-123">-H</span><span class="sxs-lookup"><span data-stu-id="9c9a4-123">-h</span></span>     |                  | <span data-ttu-id="9c9a4-124">Incluez le hachage de la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="9c9a4-124">Include the hash of the digital signature.</span></span> <span data-ttu-id="9c9a4-125">Cette étape est facultative.</span><span class="sxs-lookup"><span data-stu-id="9c9a4-125">This is optional.</span></span>                                            |



 

<span data-ttu-id="9c9a4-126">Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="9c9a4-126">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c9a4-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c9a4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c9a4-128">Outils de développement Windows Installer</span><span class="sxs-lookup"><span data-stu-id="9c9a4-128">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="9c9a4-129">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="9c9a4-129">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



