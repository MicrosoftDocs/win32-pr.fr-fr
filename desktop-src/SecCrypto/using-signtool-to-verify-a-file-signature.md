---
description: Explique comment utiliser SignTool pour vérifier une signature de fichier.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Utilisation de SignTool pour vérifier une signature de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8161d4c890400f3aa33b415e7ac16a5306aa094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518355"
---
# <a name="using-signtool-to-verify-a-file-signature"></a><span data-ttu-id="573fd-103">Utilisation de SignTool pour vérifier une signature de fichier</span><span class="sxs-lookup"><span data-stu-id="573fd-103">Using SignTool to Verify a File Signature</span></span>

<span data-ttu-id="573fd-104">La commande suivante vérifie la signature d’un fichier nommé *MyControl.exe*:</span><span class="sxs-lookup"><span data-stu-id="573fd-104">The following command verifies the signature of a file named *MyControl.exe*:</span></span>

<span data-ttu-id="573fd-105"> *MyControl.exe* de vérification de SignTool</span><span class="sxs-lookup"><span data-stu-id="573fd-105">**SignTool verify** *MyControl.exe*</span></span>

<span data-ttu-id="573fd-106">Si l’exemple précédent échoue, il se peut que la signature utilise un certificat de signature de code.</span><span class="sxs-lookup"><span data-stu-id="573fd-106">If the preceding example fails, it could be that the signature used a code-signing certificate.</span></span> <span data-ttu-id="573fd-107">[SignTool](signtool.md) est par défaut la stratégie de pilote Windows pour la vérification.</span><span class="sxs-lookup"><span data-stu-id="573fd-107">[SignTool](signtool.md) defaults to the Windows driver policy for verification.</span></span>

<span data-ttu-id="573fd-108">La commande suivante vérifie la signature à l’aide de la stratégie de vérification d’authentification par défaut :</span><span class="sxs-lookup"><span data-stu-id="573fd-108">The following command verifies the signature, using the Default Authentication Verification Policy:</span></span>

<span data-ttu-id="573fd-109">**SignTool Verify/pa** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="573fd-109">**SignTool verify /pa** *MyControl.exe*</span></span>

<span data-ttu-id="573fd-110">La commande suivante vérifie un fichier système qui peut être signé dans un catalogue :</span><span class="sxs-lookup"><span data-stu-id="573fd-110">The following command verifies a system file that may be signed in a catalog:</span></span>

<span data-ttu-id="573fd-111">**Vérification de SignTool/a** *SysFile.dll*</span><span class="sxs-lookup"><span data-stu-id="573fd-111">**SignTool verify /a** *SysFile.dll*</span></span>

<span data-ttu-id="573fd-112">La commande suivante vérifie un fichier système qui est signé dans un catalogue nommé *MyCat.cat*:</span><span class="sxs-lookup"><span data-stu-id="573fd-112">The following command verifies a system file that is signed in a catalog named *MyCat.cat*:</span></span>

<span data-ttu-id="573fd-113">**SignTool Verify/c** *MyCat.catMyFile.ini*</span><span class="sxs-lookup"><span data-stu-id="573fd-113">**SignTool verify /c** *MyCat.catMyFile.ini*</span></span>

<span data-ttu-id="573fd-114">Pour toute vérification de [SignTool](signtool.md) , vous pouvez récupérer le signataire du certificat.</span><span class="sxs-lookup"><span data-stu-id="573fd-114">For any [SignTool](signtool.md) verification, you can retrieve the signer of the certificate.</span></span> <span data-ttu-id="573fd-115">La commande suivante vérifie un fichier système et affiche le certificat du signataire :</span><span class="sxs-lookup"><span data-stu-id="573fd-115">The following command verifies a system file and displays the signer certificate:</span></span>

<span data-ttu-id="573fd-116">**SignTool Verify/v** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="573fd-116">**SignTool verify /v** *MyControl.exe*</span></span>

<span data-ttu-id="573fd-117">[SignTool](signtool.md) retourne le texte de ligne de commande qui indique le résultat de la vérification de signature.</span><span class="sxs-lookup"><span data-stu-id="573fd-117">[SignTool](signtool.md) returns command-line text that states the result of the signature check.</span></span> <span data-ttu-id="573fd-118">En outre, SignTool retourne un code de sortie de zéro pour une exécution réussie, un pour l’échec de l’exécution et deux pour l’exécution qui s’est terminée avec des avertissements.</span><span class="sxs-lookup"><span data-stu-id="573fd-118">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="573fd-119">Pour plus d’informations sur [SignTool](signtool.md), consultez [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="573fd-119">For more information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 



