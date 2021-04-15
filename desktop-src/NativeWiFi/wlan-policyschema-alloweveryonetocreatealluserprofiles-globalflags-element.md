---
description: Spécifie si un utilisateur peut créer un profil tous les utilisateurs.
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: Élément allowEveryoneToCreateAllUserProfiles (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowEveryoneToCreateAllUserProfiles
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 63bc4c76ccecd8c7f774dc0e73621ef3f9b19877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525767"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a><span data-ttu-id="45737-103">Élément allowEveryoneToCreateAllUserProfiles (globalFlags)</span><span class="sxs-lookup"><span data-stu-id="45737-103">allowEveryoneToCreateAllUserProfiles (globalFlags) Element</span></span>

<span data-ttu-id="45737-104">L’élément **allowEveryoneToCreateAllUserProfiles** (globalFlags) spécifie si un utilisateur peut créer un profil All-User.</span><span class="sxs-lookup"><span data-stu-id="45737-104">The **allowEveryoneToCreateAllUserProfiles** (globalFlags) element specifies whether any user can create an all-user profile.</span></span> <span data-ttu-id="45737-105">Un profil tous les utilisateurs peut être utilisé par n’importe quel utilisateur sur l’ordinateur pour se connecter au réseau sans fil associé au profil.</span><span class="sxs-lookup"><span data-stu-id="45737-105">An all-user profile can be used by any user on the machine to connect to the wireless network associated with the profile.</span></span>

<span data-ttu-id="45737-106">Si **allowEveryoneToCreateAllUserProfiles** a la valeur true, les utilisateurs peuvent créer un profil All-User.</span><span class="sxs-lookup"><span data-stu-id="45737-106">If **allowEveryoneToCreateAllUserProfiles** is TRUE, than any user can create an all-user profile.</span></span> <span data-ttu-id="45737-107">Si **allowEveryoneToCreateAllUserProfiles** a la valeur false, tous les utilisateurs ne peuvent pas créer un profil All-User, et il existe une liste DACL associée à l' \_ objet de sécurité WLAN Secure \_ Add \_ New \_ All \_ User \_ Profiles qui spécifie les utilisateurs ou les groupes d’utilisateurs autorisés à créer des profils tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="45737-107">If **allowEveryoneToCreateAllUserProfiles** is FALSE, then not all users can create an all-user profile, and there is a DACL associated with the wlan\_secure\_add\_new\_all\_user\_profiles security object that specifies the users or user groups with permission to create all-user profiles.</span></span> <span data-ttu-id="45737-108">La liste DACL par défaut spécifie que seuls les utilisateurs ayant ouvert une session en tant que membre du groupe administrateurs peuvent créer un profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="45737-108">The default DACL specifies that only users that are logged on as a member of the Administrators group can create an all-user profile.</span></span> <span data-ttu-id="45737-109">Les paramètres de sécurité par défaut peuvent être modifiés en appelant [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="45737-109">The default security settings can be changed by calling [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings).</span></span> <span data-ttu-id="45737-110">Pour accéder aux paramètres de sécurité actuels, appelez [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="45737-110">To get the current security settings, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="45737-111">Cet élément est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="45737-111">This element is mandatory.</span></span> <span data-ttu-id="45737-112">Lorsqu’un profil est créé par le service de configuration automatique, cet élément a la valeur par défaut TRUE.</span><span class="sxs-lookup"><span data-stu-id="45737-112">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

<span data-ttu-id="45737-113">L’élément **allowEveryoneToCreateAllUserProfiles** est défini par l’élément [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="45737-113">The **allowEveryoneToCreateAllUserProfiles** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="45737-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45737-114">Requirements</span></span>



| <span data-ttu-id="45737-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45737-115">Requirement</span></span> | <span data-ttu-id="45737-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="45737-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="45737-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45737-117">Minimum supported client</span></span><br/> | <span data-ttu-id="45737-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45737-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="45737-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45737-119">Minimum supported server</span></span><br/> | <span data-ttu-id="45737-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45737-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45737-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45737-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="45737-122">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="45737-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="45737-123">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="45737-123">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="45737-124">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="45737-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="45737-125">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="45737-125">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




