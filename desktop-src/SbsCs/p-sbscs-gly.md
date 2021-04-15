---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (applications isolées et assemblys côte à côte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c70c0775af4a6245e74de474413c3741625456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393359"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="d94c9-103">P (applications isolées et assemblys côte à côte)</span><span class="sxs-lookup"><span data-stu-id="d94c9-103">P (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="d94c9-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) e F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="d94c9-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d94c9-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**configuration par application**</span><span class="sxs-lookup"><span data-stu-id="d94c9-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**per-application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="d94c9-106">Configuration qui peut remplacer la configuration d’application globale d’un assembly spécifique.</span><span class="sxs-lookup"><span data-stu-id="d94c9-106">Configuration that can override a specific assembly's global application configuration.</span></span> <span data-ttu-id="d94c9-107">Une configuration par application est spécifiée par un fichier manifeste de configuration de l’application installé dans le même dossier que le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="d94c9-107">A per-application configuration is specified by an application configuration manifest file installed in the same folder as the executable file.</span></span> <span data-ttu-id="d94c9-108">Le fichier manifeste décrit la version, ou la plage de versions, des assemblys côte à côte devant être utilisés par l’application.</span><span class="sxs-lookup"><span data-stu-id="d94c9-108">The manifest file describes the version, or range of versions, of side-by-side assemblies to be used by the application.</span></span> <span data-ttu-id="d94c9-109">La configuration par application peut être utilisée quand une nouvelle version d’un assembly est incompatible avec une application.</span><span class="sxs-lookup"><span data-stu-id="d94c9-109">Per-application configuration might be used when a new version of an assembly is incompatible with an application.</span></span> <span data-ttu-id="d94c9-110">Dans ce cas, la configuration globale ou par défaut de l’application peut être remplacée pour un assembly côte à côte spécifique.</span><span class="sxs-lookup"><span data-stu-id="d94c9-110">In this case, the application's default or global configuration can be overridden for a specific side-by-side assembly.</span></span>

</dd> <dt>

<span data-ttu-id="d94c9-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly côte à côte privé**</span><span class="sxs-lookup"><span data-stu-id="d94c9-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**private side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="d94c9-112">Un assembly côte à côte privé est uniquement visible pour une application spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d94c9-112">A private side-by-side assembly is only visible to a specified application.</span></span> <span data-ttu-id="d94c9-113">Il est installé localement dans une application isolée et le code de l’assembly devient privé dans le contexte de l’application.</span><span class="sxs-lookup"><span data-stu-id="d94c9-113">It is installed locally to an isolated application and the assembly's code becomes private to the application context.</span></span> <span data-ttu-id="d94c9-114">Les dépendances d’un assembly côte à côte privé sont décrites dans le fichier manifeste de l’application.</span><span class="sxs-lookup"><span data-stu-id="d94c9-114">The dependencies of a private side-by-side assembly are described in the application manifest file.</span></span> <span data-ttu-id="d94c9-115">Les assemblys côte à côte privés peuvent être utilisés pour décaler les effets négatifs du partage d’assembly, tels que les conflits de DLL, et pour faciliter le déploiement d’applications.</span><span class="sxs-lookup"><span data-stu-id="d94c9-115">Private side-by-side assemblies can be used to offset the negative effects of assembly sharing, such as DLL conflicts, and to facilitate application deployment.</span></span>

</dd> <dt>

<span data-ttu-id="d94c9-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**jeton de clé publique**</span><span class="sxs-lookup"><span data-stu-id="d94c9-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**public key token**</span></span>
</dt> <dd>

<span data-ttu-id="d94c9-117">Chaîne hexadécimale de 16 caractères qui représente les 8 derniers octets du hachage SHA-1 de la clé publique sous laquelle l’assembly est signé.</span><span class="sxs-lookup"><span data-stu-id="d94c9-117">A 16-character hexadecimal string that represents the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="d94c9-118">La clé publique utilisée pour signer le catalogue doit être supérieure ou égale à 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="d94c9-118">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="d94c9-119">Obligatoire pour tous les assemblys côte à côte partagés.</span><span class="sxs-lookup"><span data-stu-id="d94c9-119">Required for all shared side-by-side assemblies.</span></span>

</dd> </dl>

 

 



