---
description: La conception de SSPI permet d’écrire et d’ajouter des SSP supplémentaires au système.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Écriture et installation d’un fournisseur de support de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526123"
---
# <a name="writing-and-installing-a-security-support-provider"></a><span data-ttu-id="87465-103">Écriture et installation d’un fournisseur de support de sécurité</span><span class="sxs-lookup"><span data-stu-id="87465-103">Writing and Installing a Security Support Provider</span></span>

<span data-ttu-id="87465-104">La conception de SSPI permet d’écrire et d’ajouter des SSP supplémentaires au système.</span><span class="sxs-lookup"><span data-stu-id="87465-104">The design of SSPI enables additional SSPs to be written and added to the system.</span></span> <span data-ttu-id="87465-105">Un [*SSP*](../secgloss/s-gly.md) spécifique à un modèle de sécurité peut être développé avec une simplicité ou une complexité relativement importante, selon le niveau d’intégration avec le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="87465-105">An [*SSP*](../secgloss/s-gly.md) specific to a security model can be developed with relative ease or great complexity, depending on the level of integration with the operating system.</span></span> <span data-ttu-id="87465-106">Un fournisseur SSP client qui autorise les connexions à un nouveau type de serveur peut être développé très rapidement, alors qu’un SSP complet qui fournit l’emprunt d’identité local nécessiterait plus d’efforts.</span><span class="sxs-lookup"><span data-stu-id="87465-106">A client SSP that allows connections to a new type of server could be developed very quickly, whereas a full SSP that provides local impersonation would require more effort.</span></span>

<span data-ttu-id="87465-107">Les SSP sont installés en mettant à jour une valeur **reg \_ SZ** dans le registre, comme suit :</span><span class="sxs-lookup"><span data-stu-id="87465-107">SSPs are installed by updating a **REG\_SZ** value in the registry, located as follows:</span></span>

<span data-ttu-id="87465-108">**HKEY \_ \_** \\Provider1.dll du contrôle CurrentControlSet du **système** de l’ordinateur local \\  \\  \\ **SecurityProviders**  =  *, Provider2.dll*    </span><span class="sxs-lookup"><span data-stu-id="87465-108">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **SecurityProviders** = *Provider1.dll, Provider2.dll,*…</span></span><dl> <dt>

            Data type
</dt> <dd>            <span data-ttu-id="87465-109">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="87465-109">REG\_SZ</span></span></dd> </dl>

<span data-ttu-id="87465-110">Une seule DLL peut contenir plusieurs SSP.</span><span class="sxs-lookup"><span data-stu-id="87465-110">A single DLL can contain multiple SSPs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87465-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87465-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87465-112">Restrictions concernant l’inscription et l’installation d’un package de sécurité</span><span class="sxs-lookup"><span data-stu-id="87465-112">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
