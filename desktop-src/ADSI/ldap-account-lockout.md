---
title: Verrouillage de compte (fournisseur LDAP)
description: Lorsque le nombre d’échecs de tentative de connexion est dépassé, le compte d’utilisateur est verrouillé pendant une période spécifiée par l’attribut lockoutDuration.
ms.assetid: bf86f6ac-8209-4306-8736-99ce53c93617
ms.tgt_platform: multiple
keywords:
- Verrouillage de compte (fournisseur LDAP)
- Verrouillage de compte ADSI, fournisseur LDAP
- ADSI Provider ADSI, exemples de gestion des utilisateurs, verrouillage de compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b7a25943debfd08469ce9a28463c88159ded9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106538601"
---
# <a name="account-lockout-ldap-provider"></a><span data-ttu-id="16073-106">Verrouillage de compte (fournisseur LDAP)</span><span class="sxs-lookup"><span data-stu-id="16073-106">Account Lockout (LDAP Provider)</span></span>

<span data-ttu-id="16073-107">Lorsque le nombre d’échecs de tentative de connexion est dépassé, le compte d’utilisateur est verrouillé pendant une période spécifiée par l’attribut [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) .</span><span class="sxs-lookup"><span data-stu-id="16073-107">When the number of failed logon attempts is exceeded, the user account is locked out for a time period specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="16073-108">La propriété [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) semble être la propriété à utiliser pour lire et modifier l’état de verrouillage d’un compte d’utilisateur, mais le fournisseur ADSI LDAP ne prend pas en charge avec précision la propriété **IsAccountLocked** .</span><span class="sxs-lookup"><span data-stu-id="16073-108">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the LDAP ADSI provider does not accurately support the **IsAccountLocked** property.</span></span> <span data-ttu-id="16073-109">Pour obtenir et définir des données de verrouillage de compte précises, utilisez le fournisseur Winnt.</span><span class="sxs-lookup"><span data-stu-id="16073-109">To obtain and set accurate account lockout data, use the WinNT provider.</span></span> <span data-ttu-id="16073-110">Pour plus d’informations sur l’utilisation de la propriété **IsAccountLocked** avec le fournisseur WinNT, consultez [verrouillage de compte (fournisseur WinNT)](winnt-account-lockout.md).</span><span class="sxs-lookup"><span data-stu-id="16073-110">For more information about using the **IsAccountLocked** property with the WinNT provider, see [Account Lockout (WinNT Provider)](winnt-account-lockout.md).</span></span>

 

 