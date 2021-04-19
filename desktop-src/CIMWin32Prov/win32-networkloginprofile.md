---
description: Le \_ NetworkLoginProfile Win32&\# 8194 ; La classe WMI représente les informations de connexion réseau d’un utilisateur spécifique sur un système informatique exécutant Windows.
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Classe Win32_NetworkLoginProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b138ce4bc92088896286f4a21a039b068e2206e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514360"
---
# <a name="win32_networkloginprofile-class"></a><span data-ttu-id="e086e-103">\_Classe NetworkLoginProfile Win32</span><span class="sxs-lookup"><span data-stu-id="e086e-103">Win32\_NetworkLoginProfile class</span></span>

<span data-ttu-id="e086e-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkLoginProfile** WMI représente les informations de connexion réseau d’un utilisateur spécifique sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="e086e-104">The **Win32\_NetworkLoginProfile** [WMI class](../wmisdk/retrieving-a-class.md) represents the network login information of a specific user on a computer system running Windows.</span></span> <span data-ttu-id="e086e-105">Cela comprend, mais ne se limite pas à l’état du mot de passe, les privilèges d’accès, les quotas de disque et les chemins d’accès aux répertoires de connexion.</span><span class="sxs-lookup"><span data-stu-id="e086e-105">This includes, but is not limited to password status, access privileges, disk quotas, and logon directory paths.</span></span>

<span data-ttu-id="e086e-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e086e-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e086e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e086e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a><span data-ttu-id="e086e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e086e-108">Members</span></span>

<span data-ttu-id="e086e-109">La classe **Win32 \_ NetworkLoginProfile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e086e-109">The **Win32\_NetworkLoginProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="e086e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e086e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e086e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e086e-111">Properties</span></span>

<span data-ttu-id="e086e-112">La classe **Win32 \_ NetworkLoginProfile** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e086e-112">The **Win32\_NetworkLoginProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e086e-113">**AccountExpires dans**</span><span class="sxs-lookup"><span data-stu-id="e086e-113">**AccountExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-114">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e086e-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-116">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ compte \_ expire »)</span><span class="sxs-lookup"><span data-stu-id="e086e-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_acct\_expires")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-117">Le compte va expirer.</span><span class="sxs-lookup"><span data-stu-id="e086e-117">Account will expire.</span></span> <span data-ttu-id="e086e-118">Cette valeur est calculée à partir du nombre de secondes écoulées depuis le 00:00:00, le 1er janvier 1970, et est défini au format suivant : AAAAMMJJHHMMSS. mmmmmm sutc.</span><span class="sxs-lookup"><span data-stu-id="e086e-118">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970, and is set in this format: yyyymmddhhmmss.mmmmmm sutc.</span></span>

<span data-ttu-id="e086e-119">Exemple : 20521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="e086e-119">Example: 20521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="e086e-120">**AuthorizationFlags**</span><span class="sxs-lookup"><span data-stu-id="e086e-120">**AuthorizationFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-121">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e086e-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-123">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ auth \_ Flags »), [**bitvalues**](../wmisdk/standard-qualifiers.md) (« Printer », « communication », « Server », « Accounts »)</span><span class="sxs-lookup"><span data-stu-id="e086e-123">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_auth\_flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-124">Ensemble d’indicateurs qui spécifient les ressources qu’un utilisateur est autorisé à utiliser ou modifier.</span><span class="sxs-lookup"><span data-stu-id="e086e-124">Set of flags that specify the resources a user is authorized to use or modify.</span></span>

<dt>

<span data-ttu-id="e086e-125">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="e086e-125">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-126">Imprimante</span><span class="sxs-lookup"><span data-stu-id="e086e-126">Printer</span></span>

</dd> <dt>

<span data-ttu-id="e086e-127">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="e086e-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-128">Communication</span><span class="sxs-lookup"><span data-stu-id="e086e-128">Communication</span></span>

</dd> <dt>

<span data-ttu-id="e086e-129">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="e086e-129">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-130">Serveur</span><span class="sxs-lookup"><span data-stu-id="e086e-130">Server</span></span>

</dd> <dt>

<span data-ttu-id="e086e-131">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="e086e-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-132">Comptes</span><span class="sxs-lookup"><span data-stu-id="e086e-132">Accounts</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e086e-133">**BadPasswordCount**</span><span class="sxs-lookup"><span data-stu-id="e086e-133">**BadPasswordCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e086e-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-136">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management Functions \| NetUserEnum »)</span><span class="sxs-lookup"><span data-stu-id="e086e-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|NetUserEnum")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-137">Nombre de fois où l’utilisateur entre un mot de passe incorrect lors de la connexion à un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="e086e-137">Number of times the user enters a bad password when logging on to a computer system running Windows.</span></span>

<span data-ttu-id="e086e-138">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="e086e-138">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="e086e-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e086e-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-142">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="e086e-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e086e-143">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="e086e-143">Short textual description of the current object.</span></span>

<span data-ttu-id="e086e-144">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e086e-144">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e086e-145">**CodePage**</span><span class="sxs-lookup"><span data-stu-id="e086e-145">**CodePage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e086e-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-148">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 page de \_ codes \_ »)</span><span class="sxs-lookup"><span data-stu-id="e086e-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_code\_page")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-149">Page de codes pour le langage de votre choix.</span><span class="sxs-lookup"><span data-stu-id="e086e-149">Code page for the user's language of choice.</span></span> <span data-ttu-id="e086e-150">Une page de codes est le jeu de caractères utilisé.</span><span class="sxs-lookup"><span data-stu-id="e086e-150">A code page is the character set used.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-151">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e086e-151">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-154">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Comment »)</span><span class="sxs-lookup"><span data-stu-id="e086e-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-155">Commentaire ou description pour ce profil d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="e086e-155">Comment or description for this logon profile.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-156">**CountryCode**</span><span class="sxs-lookup"><span data-stu-id="e086e-156">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e086e-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-159">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Country \_ Code »)</span><span class="sxs-lookup"><span data-stu-id="e086e-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_country\_code")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-160">Code de pays/région pour la langue choisie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-160">Country/region code for the user's language of choice.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-161">**Description**</span><span class="sxs-lookup"><span data-stu-id="e086e-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e086e-164">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="e086e-164">Textual description of the current object.</span></span>

<span data-ttu-id="e086e-165">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e086e-165">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e086e-166">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="e086e-166">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-167">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e086e-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-169">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags »), [**bitmap**](../wmisdk/standard-qualifiers.md) (« 0 », « 1 "," 3 "," 4 "," 5 "," 6 "," 7 "," 8 "," 9 "," 11 "," 12 "," 13 "," 16 "," 17 "," 18 "," 19 "," 20 "," 21 "," 22 "," 23 "), [**BitValue**](../wmisdk/standard-qualifiers.md) (" script "," compte désactivé "," répertoire de départ requis "," verrouillage "," mot de passe non requis "," Paswword ne peut pas changer "," mot de passe de test chiffré autorisé "," compte Temp dupliqué "," compte normal "," compte de confiance interdomaine ", «compte d’approbation de station de travail », « compte de confiance de serveur », « ne pas faire expirer le mot de passe », « compte d’ouverture de session MNS », « carte à puce requise », « approuvé pour la délégation », « non délégué », « utiliser la clé des uniquement », « ne pas exiger une pré-autorisation »</span><span class="sxs-lookup"><span data-stu-id="e086e-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags"), [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Script", "Account Disabled", "Home Dir Required", "Lockout", "Password Not Required", "Paswword Can't Change", "Encrypted Test Password Allowed", "Temp Duplicate Account", "Normal Account", "InterDomain Trust Account", "WorkStation Trust Account", "Server Trust Account", "Don't Expire Password", "MNS Logon Account", "Smartcard Required", "Trusted For Delegation", "Not Delegated", "Use DES Key Only", "Don't Require Preauthorization", "Password Expired")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-170">Propriétés disponibles pour ce profil réseau.</span><span class="sxs-lookup"><span data-stu-id="e086e-170">The properties available to this network profile.</span></span>

<span data-ttu-id="e086e-171">Les propriétés qui peuvent être définies sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e086e-171">Properties that can be set include:</span></span>

<dt>

<span data-ttu-id="e086e-172">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="e086e-172">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-173">Script</span><span class="sxs-lookup"><span data-stu-id="e086e-173">Script</span></span>

<span data-ttu-id="e086e-174">Un script d’ouverture de session exécuté.</span><span class="sxs-lookup"><span data-stu-id="e086e-174">A logon script executed.</span></span> <span data-ttu-id="e086e-175">Cette valeur doit être définie pour LAN Manager 2,0.</span><span class="sxs-lookup"><span data-stu-id="e086e-175">This value must be set for LAN Manager 2.0.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-176">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="e086e-176">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-177">Compte désactivé</span><span class="sxs-lookup"><span data-stu-id="e086e-177">Account Disabled</span></span>

<span data-ttu-id="e086e-178">Le compte de l’utilisateur est désactivé.</span><span class="sxs-lookup"><span data-stu-id="e086e-178">The user's account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-179">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="e086e-179">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-180">Répertoire de démarrage requis</span><span class="sxs-lookup"><span data-stu-id="e086e-180">Home Directory Required</span></span>

<span data-ttu-id="e086e-181">Un répertoire de départ est requis.</span><span class="sxs-lookup"><span data-stu-id="e086e-181">A home directory is required.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-182">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="e086e-182">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-183">Verrouillage.</span><span class="sxs-lookup"><span data-stu-id="e086e-183">Lockout</span></span>

<span data-ttu-id="e086e-184">Le compte est actuellement verrouillé. Pour [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), cette valeur peut être désactivée pour déverrouiller un compte précédemment verrouillé.</span><span class="sxs-lookup"><span data-stu-id="e086e-184">The account is currently locked out. For [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), this value can be cleared to unlock a previously locked account.</span></span> <span data-ttu-id="e086e-185">Cette valeur ne peut pas être utilisée pour verrouiller un compte précédemment déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="e086e-185">This value cannot be used to lock a previously unlocked account.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-186">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="e086e-186">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-187">Mot de passe non requis</span><span class="sxs-lookup"><span data-stu-id="e086e-187">Password Not Required</span></span>

<span data-ttu-id="e086e-188">Aucun mot de passe n'est requis.</span><span class="sxs-lookup"><span data-stu-id="e086e-188">No password is required.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-189">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="e086e-189">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-190">Le mot de passe ne peut pas être modifié</span><span class="sxs-lookup"><span data-stu-id="e086e-190">Password Cannot Change</span></span>

<span data-ttu-id="e086e-191">L’utilisateur ne peut pas modifier le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="e086e-191">The user cannot change the password.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-192">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="e086e-192">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-193">Mot de passe de test chiffré autorisé</span><span class="sxs-lookup"><span data-stu-id="e086e-193">Encrypted Test Password Allowed</span></span>

</dd> <dt>

<span data-ttu-id="e086e-194">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="e086e-194">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-195">Compte temporaire dupliqué</span><span class="sxs-lookup"><span data-stu-id="e086e-195">Temp Duplicate Account</span></span>

<span data-ttu-id="e086e-196">Compte pour les utilisateurs dont le compte principal se trouve dans un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="e086e-196">An account for users whose primary account is in another domain.</span></span> <span data-ttu-id="e086e-197">Ce compte fournit l’accès utilisateur à ce domaine, mais pas à un domaine qui approuve ce domaine.</span><span class="sxs-lookup"><span data-stu-id="e086e-197">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="e086e-198">Le gestionnaire de l’utilisateur fait référence à ce type de compte en tant que compte d’utilisateur local.</span><span class="sxs-lookup"><span data-stu-id="e086e-198">The User Manager refers to this account type as a local user account.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-199">512 (0x200)</span><span class="sxs-lookup"><span data-stu-id="e086e-199">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-200">Compte normal</span><span class="sxs-lookup"><span data-stu-id="e086e-200">Normal Account</span></span>

<span data-ttu-id="e086e-201">Type de compte par défaut qui représente un utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="e086e-201">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-202">2048 (0x800)</span><span class="sxs-lookup"><span data-stu-id="e086e-202">2048 (0x800)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-203">Compte de confiance interdomaine</span><span class="sxs-lookup"><span data-stu-id="e086e-203">Interdomain Trust Account</span></span>

<span data-ttu-id="e086e-204">Autorisation à un compte de confiance pour un domaine qui approuve d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="e086e-204">A permit to a trust account for a domain that trusts other domains.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-205">4096 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="e086e-205">4096 (0x1000)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-206">Compte d’approbation de station de travail</span><span class="sxs-lookup"><span data-stu-id="e086e-206">Workstation Trust Account</span></span>

<span data-ttu-id="e086e-207">Un compte d’ordinateur pour une station de travail ou un serveur Windows qui est membre de ce domaine.</span><span class="sxs-lookup"><span data-stu-id="e086e-207">A computer account for a Windows workstation or server that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-208">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="e086e-208">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-209">Compte de confiance du serveur</span><span class="sxs-lookup"><span data-stu-id="e086e-209">Server Trust Account</span></span>

<span data-ttu-id="e086e-210">Un compte d’ordinateur pour un contrôleur de domaine de sauvegarde qui est membre de ce domaine.</span><span class="sxs-lookup"><span data-stu-id="e086e-210">A computer account for a backup domain controller that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-211">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="e086e-211">65536 (0x10000)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-212">Ne pas faire expirer le mot de passe</span><span class="sxs-lookup"><span data-stu-id="e086e-212">Do Not Expire Password</span></span>

</dd> <dt>

<span data-ttu-id="e086e-213">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="e086e-213">131072 (0x20000)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-214">Compte d’ouverture de session MNS</span><span class="sxs-lookup"><span data-stu-id="e086e-214">MNS Logon Account</span></span>

<span data-ttu-id="e086e-215">Type de compte d’ouverture de session jeu de nœud majoritaire (MNS) qui représente un utilisateur MNS.</span><span class="sxs-lookup"><span data-stu-id="e086e-215">Majority Node Set (MNS) logon account type that represents an MNS user.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-216">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="e086e-216">262144 (0x40000)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-217">Carte à puce requise</span><span class="sxs-lookup"><span data-stu-id="e086e-217">Smartcard Required</span></span>

</dd> <dt>

<span data-ttu-id="e086e-218">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="e086e-218">524288 (0x80000)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-219">Approuvé pour la délégation</span><span class="sxs-lookup"><span data-stu-id="e086e-219">Trusted for Delegation</span></span>

</dd> <dt>

<span data-ttu-id="e086e-220">1048576 ()</span><span class="sxs-lookup"><span data-stu-id="e086e-220">1048576 (0x100000)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-221">Non délégué</span><span class="sxs-lookup"><span data-stu-id="e086e-221">Not Delegated</span></span>

</dd> <dt>

<span data-ttu-id="e086e-222">2097152 (0x200000)</span><span class="sxs-lookup"><span data-stu-id="e086e-222">2097152 (0x200000)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-223">Utiliser la clé DES uniquement</span><span class="sxs-lookup"><span data-stu-id="e086e-223">Use DES Key Only</span></span>

</dd> <dt>

<span data-ttu-id="e086e-224">4194304 (0x400000)</span><span class="sxs-lookup"><span data-stu-id="e086e-224">4194304 (0x400000)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-225">Ne pas exiger la pré-autorisation</span><span class="sxs-lookup"><span data-stu-id="e086e-225">Do Not Require Preauthorization</span></span>

</dd> <dt>

<span data-ttu-id="e086e-226">8388608 (0x800000)</span><span class="sxs-lookup"><span data-stu-id="e086e-226">8388608 (0x800000)</span></span>
</dt> <dd>

<span data-ttu-id="e086e-227">Mot de passe expiré</span><span class="sxs-lookup"><span data-stu-id="e086e-227">Password Expired</span></span>

<span data-ttu-id="e086e-228">Indique que le mot de passe a expiré.</span><span class="sxs-lookup"><span data-stu-id="e086e-228">Indicates that the password has expired.</span></span>

</dd> </dl>

<span data-ttu-id="e086e-229">Les propriétés suivantes décrivent le type de compte.</span><span class="sxs-lookup"><span data-stu-id="e086e-229">The following properties describe the account type.</span></span> <span data-ttu-id="e086e-230">Une seule valeur peut être définie :</span><span class="sxs-lookup"><span data-stu-id="e086e-230">Only one value can be set:</span></span>

-   <span data-ttu-id="e086e-231">\_compte standard \_ uf</span><span class="sxs-lookup"><span data-stu-id="e086e-231">UF\_NORMAL\_ACCOUNT</span></span>
-   <span data-ttu-id="e086e-232">\_ \_ compte DUPLIQUÉ temporaire \_ uf</span><span class="sxs-lookup"><span data-stu-id="e086e-232">UF\_TEMP\_DUPLICATE\_ACCOUNT</span></span>
-   <span data-ttu-id="e086e-233">compte d’approbation de station de \_ travail UF \_ \_</span><span class="sxs-lookup"><span data-stu-id="e086e-233">UF\_WORKSTATION\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="e086e-234">\_compte de \_ confiance du serveur uf \_</span><span class="sxs-lookup"><span data-stu-id="e086e-234">UF\_SERVER\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="e086e-235">\_compte de confiance interdomaine UF \_ \_</span><span class="sxs-lookup"><span data-stu-id="e086e-235">UF\_INTERDOMAIN\_TRUST\_ACCOUNT</span></span>

</dd> <dt>

<span data-ttu-id="e086e-236">**FullName**</span><span class="sxs-lookup"><span data-stu-id="e086e-236">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-239">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Full \_ Name »)</span><span class="sxs-lookup"><span data-stu-id="e086e-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_full\_name")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-240">Nom complet de l’utilisateur appartenant au profil de connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="e086e-240">Full name of the user belonging to the network login profile.</span></span> <span data-ttu-id="e086e-241">Cette chaîne peut être vide si l’utilisateur choisit de ne pas associer un nom complet à un nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-241">This string can be empty if the user chooses not to associate a full name with a user name.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-242">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="e086e-242">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-245">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ orig \_ dir »)</span><span class="sxs-lookup"><span data-stu-id="e086e-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-246">Chemin d’accès au répertoire de départ de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-246">Path to the home directory of the user.</span></span> <span data-ttu-id="e086e-247">Cette chaîne peut être vide si l’utilisateur choisit de ne pas spécifier de répertoire de démarrage.</span><span class="sxs-lookup"><span data-stu-id="e086e-247">This string may be empty if the user chooses not to specify a home directory.</span></span>

<span data-ttu-id="e086e-248">Exemple : « \\ homedir »</span><span class="sxs-lookup"><span data-stu-id="e086e-248">Example:"\\HOMEDIR"</span></span>

</dd> <dt>

<span data-ttu-id="e086e-249">**HomeDirectoryDrive**</span><span class="sxs-lookup"><span data-stu-id="e086e-249">**HomeDirectoryDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-250">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-252">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ orig \_ dir \_ Drive »)</span><span class="sxs-lookup"><span data-stu-id="e086e-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir\_drive")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-253">Lettre de lecteur affectée au répertoire de démarrage de l’utilisateur pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="e086e-253">Drive letter assigned to the user's home directory for log on purposes.</span></span>

<span data-ttu-id="e086e-254">Exemple : "C :"</span><span class="sxs-lookup"><span data-stu-id="e086e-254">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="e086e-255">**LastLogoff**</span><span class="sxs-lookup"><span data-stu-id="e086e-255">**LastLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-256">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e086e-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-258">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Last \_ Logoff »)</span><span class="sxs-lookup"><span data-stu-id="e086e-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logoff")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-259">Dernière déconnexion du système par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-259">User last logged off the system.</span></span> <span data-ttu-id="e086e-260">Cette valeur est calculée à partir du nombre de secondes écoulées depuis le 00:00:00, le 1er janvier 1970.</span><span class="sxs-lookup"><span data-stu-id="e086e-260">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="e086e-261">La valeur « \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* » signifie que l’heure de la dernière déconnexion est inconnue.</span><span class="sxs-lookup"><span data-stu-id="e086e-261">A value of " \*\*\*\*\*\*\*\*\*\*\*\*\*\*.\*\*\*\*\*\*+\*\*\* " means that the last logoff time is unknown.</span></span> <span data-ttu-id="e086e-262">Le format de cette valeur est AAAAMMJJHHMMSS. mmmmmm sutc.</span><span class="sxs-lookup"><span data-stu-id="e086e-262">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="e086e-263">Pour plus d’informations sur la traduction de cette propriété en heure locale, consultez [tâches WMI : dates et heures](../wmisdk/wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="e086e-263">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="e086e-264">Exemple : 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="e086e-264">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="e086e-265">**LastLogon**</span><span class="sxs-lookup"><span data-stu-id="e086e-265">**LastLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-266">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e086e-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-268">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Last \_ Logon »)</span><span class="sxs-lookup"><span data-stu-id="e086e-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logon")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-269">Dernier utilisateur ayant ouvert une session sur le système.</span><span class="sxs-lookup"><span data-stu-id="e086e-269">User last logged on to the system.</span></span> <span data-ttu-id="e086e-270">Cette valeur est calculée à partir du nombre de secondes écoulées depuis le 00:00:00, le 1er janvier 1970.</span><span class="sxs-lookup"><span data-stu-id="e086e-270">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="e086e-271">Le format de cette valeur est AAAAMMJJHHMMSS. mmmmmm sutc.</span><span class="sxs-lookup"><span data-stu-id="e086e-271">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="e086e-272">Pour plus d’informations sur la traduction de cette propriété en heure locale, consultez [tâches WMI : dates et heures](../wmisdk/wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="e086e-272">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="e086e-273">Exemple : 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="e086e-273">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="e086e-274">**LogonHours**</span><span class="sxs-lookup"><span data-stu-id="e086e-274">**LogonHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-275">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-277">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ hours")</span><span class="sxs-lookup"><span data-stu-id="e086e-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_hours")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-278">Heures de la semaine auxquelles l’utilisateur peut se connecter.</span><span class="sxs-lookup"><span data-stu-id="e086e-278">Times during the week when the user can log on.</span></span> <span data-ttu-id="e086e-279">Chaque bit représente une unité de temps spécifiée par la propriété **UnitsPerWeek** .</span><span class="sxs-lookup"><span data-stu-id="e086e-279">Each bit represents a unit of time specified by the **UnitsPerWeek** property.</span></span> <span data-ttu-id="e086e-280">Par exemple, si l’unité de temps est horaire, le premier bit (bit 0, mot 0) est dimanche, 0:00 à 0:59, le deuxième bit (bit 1, mot 0) est dimanche, 1:00 à 1:59, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e086e-280">For instance, if the unit of time is hourly, the first bit (bit 0, word 0) is Sunday, 0:00 to 0:59, the second bit (bit 1, word 0) is Sunday, 1:00 to 1:59, and so on.</span></span> <span data-ttu-id="e086e-281">Si ce membre a la valeur **null**, il n’y a aucune restriction de temps.</span><span class="sxs-lookup"><span data-stu-id="e086e-281">If this member is set to **NULL**, then there is no time restriction.</span></span> <span data-ttu-id="e086e-282">L’heure est définie sur GMT et doit être ajustée pour les autres fuseaux horaires (par exemple, GMT moins 8 heures pour PST).</span><span class="sxs-lookup"><span data-stu-id="e086e-282">The time is set to GMT and must be adjusted for other time zones (for example, GMT minus 8 hours for PST).</span></span>

</dd> <dt>

<span data-ttu-id="e086e-283">**LogonServer**</span><span class="sxs-lookup"><span data-stu-id="e086e-283">**LogonServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-284">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-286">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ Server »)</span><span class="sxs-lookup"><span data-stu-id="e086e-286">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_server")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-287">Nom du serveur auquel les demandes d’ouverture de session sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="e086e-287">Name of the server to which logon requests are sent.</span></span> <span data-ttu-id="e086e-288">Les noms de serveur doivent être précédés de deux barres obliques inverses ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="e086e-288">Server names should be preceded by two backslashes (\\\\).</span></span> <span data-ttu-id="e086e-289">Un nom de serveur avec un astérisque ( \\ \\ \* ) indique que la demande d’ouverture de session peut être gérée par n’importe quel serveur d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="e086e-289">A server name with an asterisk (\\\\\*) indicates that the logon request can be handled by any logon server.</span></span> <span data-ttu-id="e086e-290">Une chaîne NULL indique que les demandes sont envoyées au contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="e086e-290">A null string indicates that requests are sent to the domain controller.</span></span>

<span data-ttu-id="e086e-291">Exemple : « \\ \\ MyServer »</span><span class="sxs-lookup"><span data-stu-id="e086e-291">Example: "\\\\MyServer"</span></span>

</dd> <dt>

<span data-ttu-id="e086e-292">**MaximumStorage**</span><span class="sxs-lookup"><span data-stu-id="e086e-292">**MaximumStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-293">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e086e-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-295">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api des \| structures de gestion de réseau \| [**\_ \_**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Max \_ Storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="e086e-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_max\_storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-296">Quantité maximale d’espace disque disponible pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-296">Maximum amount of disk space available to the user.</span></span> <span data-ttu-id="e086e-297">Si MaximumStorage est défini sur USER \_ MAXSTORAGE \_ Unlimited, l’utilisateur est autorisé à utiliser tout l’espace disque disponible.</span><span class="sxs-lookup"><span data-stu-id="e086e-297">If MaximumStorage is set to USER\_MAXSTORAGE\_UNLIMITED, the user is allowed to use all of the available disk space.</span></span>

<span data-ttu-id="e086e-298">Exemple : 10 millions</span><span class="sxs-lookup"><span data-stu-id="e086e-298">Example: 10000000</span></span>

<span data-ttu-id="e086e-299">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e086e-299">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e086e-300">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e086e-300">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-303">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Name")</span><span class="sxs-lookup"><span data-stu-id="e086e-303">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_name")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-304">Compte d’utilisateur sur un domaine ou un ordinateur particulier.</span><span class="sxs-lookup"><span data-stu-id="e086e-304">User account on a particular domain or computer.</span></span> <span data-ttu-id="e086e-305">Le nombre de caractères dans le nom ne peut pas dépasser la valeur de UNLEN.</span><span class="sxs-lookup"><span data-stu-id="e086e-305">The number of characters in the name cannot exceed the value of UNLEN.</span></span>

<span data-ttu-id="e086e-306">Exemple : « somedomain \\ JohnDoe »</span><span class="sxs-lookup"><span data-stu-id="e086e-306">Example: "somedomain\\johndoe"</span></span>

</dd> <dt>

<span data-ttu-id="e086e-307">**NumberOfLogons**</span><span class="sxs-lookup"><span data-stu-id="e086e-307">**NumberOfLogons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-308">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e086e-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-310">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ num \_ Logons »)</span><span class="sxs-lookup"><span data-stu-id="e086e-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_num\_logons")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-311">Nombre de fois où l’utilisateur a réussi à se connecter à ce compte.</span><span class="sxs-lookup"><span data-stu-id="e086e-311">Number of successful times the user tried to log on to this account.</span></span> <span data-ttu-id="e086e-312">La valeur 0xFFFFFFFF indique que la valeur est inconnue.</span><span class="sxs-lookup"><span data-stu-id="e086e-312">A value of 0xFFFFFFFF indicates that the value is unknown.</span></span> <span data-ttu-id="e086e-313">Cette propriété est conservée séparément sur chaque contrôleur de domaine de sauvegarde (BDC) du domaine.</span><span class="sxs-lookup"><span data-stu-id="e086e-313">This property is maintained separately on each backup domain controller (BDC) in the domain.</span></span> <span data-ttu-id="e086e-314">Pour avoir une valeur précise, seule la plus grande valeur de tous les contrôleurs secondaires de domaine doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="e086e-314">To get an accurate value, only the largest value from all BDCs should be used.</span></span>

<span data-ttu-id="e086e-315">Example: 4</span><span class="sxs-lookup"><span data-stu-id="e086e-315">Example: 4</span></span>

</dd> <dt>

<span data-ttu-id="e086e-316">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="e086e-316">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-319">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ parms »)</span><span class="sxs-lookup"><span data-stu-id="e086e-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_parms")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-320">Espace réservé pour une utilisation par les applications.</span><span class="sxs-lookup"><span data-stu-id="e086e-320">Space set aside for use by applications.</span></span> <span data-ttu-id="e086e-321">Cette chaîne peut avoir la valeur null, ou elle peut avoir n’importe quel nombre de caractères avant le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="e086e-321">This string can be null, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="e086e-322">Les produits Microsoft utilisent ce membre pour stocker les informations de configuration de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-322">Microsoft products use this member to store user configuration information.</span></span> <span data-ttu-id="e086e-323">Ne modifiez pas ces informations, car cette valeur est spécifique à une application.</span><span class="sxs-lookup"><span data-stu-id="e086e-323">Do not modify this information, because this value is specific to an application.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-324">**Mot de passe**</span><span class="sxs-lookup"><span data-stu-id="e086e-324">**PasswordAge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-325">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e086e-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-327">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ password \_ Age »)</span><span class="sxs-lookup"><span data-stu-id="e086e-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_password\_age")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-328">Durée pendant laquelle un mot de passe a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="e086e-328">Length of time a password has been in effect.</span></span> <span data-ttu-id="e086e-329">Cette valeur est mesurée à partir du nombre de secondes écoulées depuis la dernière modification du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="e086e-329">This value is measured from the number of seconds elapsed since the password was last changed.</span></span>

<span data-ttu-id="e086e-330">Exemple : 00001201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="e086e-330">Example: 00001201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="e086e-331">**PasswordExpires**</span><span class="sxs-lookup"><span data-stu-id="e086e-331">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-332">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e086e-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-334">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**User \_ modals \_ info \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ Max \_ passwd passwd \_ Age »)</span><span class="sxs-lookup"><span data-stu-id="e086e-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_MODALS\_INFO\_0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0)\|usrmod0\_max\_passwd\_age")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-335">Date et heure d’expiration du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="e086e-335">Date and time the password expires.</span></span> <span data-ttu-id="e086e-336">La valeur est définie dans le format suivant : AAAAMMJJHHMMSS. mmmmmm sutc</span><span class="sxs-lookup"><span data-stu-id="e086e-336">The value is set in this format: yyyymmddhhmmss.mmmmmm sutc</span></span>

<span data-ttu-id="e086e-337">Exemple : 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="e086e-337">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="e086e-338">**PrimaryGroupId**</span><span class="sxs-lookup"><span data-stu-id="e086e-338">**PrimaryGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-339">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e086e-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-341">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 ID de \_ \_ groupe principal \_ »)</span><span class="sxs-lookup"><span data-stu-id="e086e-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_primary\_group\_id")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-342">Identificateur relatif (RID) du groupe global principal de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-342">Relative identifier (RID) of the Primary Global Group for this user.</span></span> <span data-ttu-id="e086e-343">L’identificateur vérifie le groupe principal auquel appartient le profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-343">The identifier verifies the primary group to which the user's profile belongs.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-344">**Privilèges**</span><span class="sxs-lookup"><span data-stu-id="e086e-344">**Privileges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-345">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e086e-345">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-347">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ priv »)</span><span class="sxs-lookup"><span data-stu-id="e086e-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_priv")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-348">Niveau de privilège affecté à la propriété de **\_ nom usri3** .</span><span class="sxs-lookup"><span data-stu-id="e086e-348">Level of privilege assigned to the **usri3\_name** property.</span></span>

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

<span data-ttu-id="e086e-349">**Invité** (0)</span><span class="sxs-lookup"><span data-stu-id="e086e-349">**Guest** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

<span data-ttu-id="e086e-350">**Utilisateur** (1)</span><span class="sxs-lookup"><span data-stu-id="e086e-350">**User** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

<span data-ttu-id="e086e-351">**Administrateur** (2)</span><span class="sxs-lookup"><span data-stu-id="e086e-351">**Administrator** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e086e-352">**Profil**</span><span class="sxs-lookup"><span data-stu-id="e086e-352">**Profile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-353">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-355">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ »)</span><span class="sxs-lookup"><span data-stu-id="e086e-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_profile")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-356">Chemin d’accès au profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-356">Path to the user's profile.</span></span> <span data-ttu-id="e086e-357">Cette valeur peut être une chaîne NULL, un chemin d’accès absolu local ou un chemin d’accès UNC.</span><span class="sxs-lookup"><span data-stu-id="e086e-357">This value can be a null string, a local absolute path, or a UNC path.</span></span> <span data-ttu-id="e086e-358">Un profil utilisateur contient des paramètres qui peuvent être personnalisés pour chaque utilisateur, tels que les couleurs du bureau.</span><span class="sxs-lookup"><span data-stu-id="e086e-358">A user profile contains settings that are customizable for each user such as the desktop colors.</span></span>

<span data-ttu-id="e086e-359">Exemple : « C : \\ Windows »</span><span class="sxs-lookup"><span data-stu-id="e086e-359">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="e086e-360">**ScriptPath**</span><span class="sxs-lookup"><span data-stu-id="e086e-360">**ScriptPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-363">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ script \_ Path »)</span><span class="sxs-lookup"><span data-stu-id="e086e-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_script\_path")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-364">Chemin d’accès du répertoire du script d’ouverture de session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-364">Directory path to the user's logon script.</span></span> <span data-ttu-id="e086e-365">Un script d’ouverture de session exécute automatiquement un ensemble de commandes chaque fois qu’un utilisateur se connecte à un système.</span><span class="sxs-lookup"><span data-stu-id="e086e-365">A logon script automatically executes a set of commands each time a user logs on to a system.</span></span>

<span data-ttu-id="e086e-366">Exemple : « C : \\ Win \\ Profiles \\ ThomasSteven »</span><span class="sxs-lookup"><span data-stu-id="e086e-366">Example: "C:\\win\\profiles\\ThomasSteven"</span></span>

</dd> <dt>

<span data-ttu-id="e086e-367">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="e086e-367">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-368">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-370">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="e086e-370">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e086e-371">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="e086e-371">Identifier by which the current object is known.</span></span>

<span data-ttu-id="e086e-372">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e086e-372">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e086e-373">**UnitsPerWeek**</span><span class="sxs-lookup"><span data-stu-id="e086e-373">**UnitsPerWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-374">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e086e-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-376">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Units \_ per \_ week »)</span><span class="sxs-lookup"><span data-stu-id="e086e-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_units\_per\_week")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-377">Nombre d’unités de temps où la semaine est divisée.</span><span class="sxs-lookup"><span data-stu-id="e086e-377">Number of time units the week is divided into.</span></span> <span data-ttu-id="e086e-378">Elle est utilisée avec la propriété **LogonHours** pour limiter l’accès utilisateur à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-378">It is used with the **LogonHours** property to limit user access to the computer.</span></span>

<span data-ttu-id="e086e-379">Exemple : 168 (heures par semaine)</span><span class="sxs-lookup"><span data-stu-id="e086e-379">Example: 168 (hours per week)</span></span>

</dd> <dt>

<span data-ttu-id="e086e-380">**UserComment**</span><span class="sxs-lookup"><span data-stu-id="e086e-380">**UserComment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-381">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-383">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ Comment »)</span><span class="sxs-lookup"><span data-stu-id="e086e-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_usr\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-384">Commentaire ou description défini par l’utilisateur pour ce profil.</span><span class="sxs-lookup"><span data-stu-id="e086e-384">User-defined comment or description for this profile.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-385">**UserId**</span><span class="sxs-lookup"><span data-stu-id="e086e-385">**UserId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-386">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e086e-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-388">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ User \_ ID »)</span><span class="sxs-lookup"><span data-stu-id="e086e-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_user\_id")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-389">RID de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-389">RID of the user.</span></span> <span data-ttu-id="e086e-390">L’identificateur vérifie que l’utilisateur existe et qu’il est unique à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="e086e-390">The identifier verifies that the user exists and is unique to this domain.</span></span>

</dd> <dt>

<span data-ttu-id="e086e-391">**UserType**</span><span class="sxs-lookup"><span data-stu-id="e086e-391">**UserType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-392">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-394">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags »)</span><span class="sxs-lookup"><span data-stu-id="e086e-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-395">Type de compte auquel l’utilisateur a des privilèges.</span><span class="sxs-lookup"><span data-stu-id="e086e-395">Type of account to which the user has privileges.</span></span>

<span data-ttu-id="e086e-396">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="e086e-396">The values are:</span></span>

-   <span data-ttu-id="e086e-397">« Compte normal »</span><span class="sxs-lookup"><span data-stu-id="e086e-397">"Normal Account"</span></span>
-   <span data-ttu-id="e086e-398">« Compte dupliqué »</span><span class="sxs-lookup"><span data-stu-id="e086e-398">"Duplicate Account"</span></span>
-   <span data-ttu-id="e086e-399">« Compte d’approbation de station de travail »</span><span class="sxs-lookup"><span data-stu-id="e086e-399">"Workstation Trust Account"</span></span>
-   <span data-ttu-id="e086e-400">« Compte de confiance de serveur »</span><span class="sxs-lookup"><span data-stu-id="e086e-400">"Server Trust Account"</span></span>
-   <span data-ttu-id="e086e-401">« Compte de confiance interdomaine »</span><span class="sxs-lookup"><span data-stu-id="e086e-401">"Interdomain Trust Account"</span></span>
-   <span data-ttu-id="e086e-402">Connue</span><span class="sxs-lookup"><span data-stu-id="e086e-402">"Unknown"</span></span>

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="e086e-403">**Compte normal** (« compte normal »)</span><span class="sxs-lookup"><span data-stu-id="e086e-403">**Normal Account** ("Normal Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="e086e-404">**Compte en double** (« compte dupliqué »)</span><span class="sxs-lookup"><span data-stu-id="e086e-404">**Duplicate Account** ("Duplicate Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="e086e-405">**Compte de confiance de station de travail** (« compte d’approbation de station de travail »)</span><span class="sxs-lookup"><span data-stu-id="e086e-405">**Workstation Trust Account** ("Workstation Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="e086e-406">**Compte de confiance de serveur** (« compte de confiance de serveur »)</span><span class="sxs-lookup"><span data-stu-id="e086e-406">**Server Trust Account** ("Server Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="e086e-407">**Compte de confiance interdomaine** (« compte de confiance interdomaine »)</span><span class="sxs-lookup"><span data-stu-id="e086e-407">**Interdomain Trust Account** ("Interdomain Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e086e-408">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="e086e-408">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e086e-409">**Stations**</span><span class="sxs-lookup"><span data-stu-id="e086e-409">**Workstations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e086e-410">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e086e-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e086e-411">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e086e-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e086e-412">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 stations de \_ travail »)</span><span class="sxs-lookup"><span data-stu-id="e086e-412">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_workstations")</span></span>
</dt> </dl>

<span data-ttu-id="e086e-413">Noms des postes de travail à partir desquels l’utilisateur peut ouvrir une session.</span><span class="sxs-lookup"><span data-stu-id="e086e-413">Names of workstations from which the user can log on.</span></span> <span data-ttu-id="e086e-414">Vous pouvez spécifier jusqu’à huit stations de travail ; les noms doivent être séparés par des virgules (,).</span><span class="sxs-lookup"><span data-stu-id="e086e-414">Up to eight workstations can be specified; the names must be separated by commas (,).</span></span> <span data-ttu-id="e086e-415">Une chaîne NULL indique qu’il n’y A aucune restriction.</span><span class="sxs-lookup"><span data-stu-id="e086e-415">A null string indicates no restrictions.</span></span> <span data-ttu-id="e086e-416">Pour désactiver les ouvertures de session de toutes les stations de travail de ce compte, définissez la valeur UF \_ ACCOUNTDISABLE dans la propriété **Flags** de cette classe.</span><span class="sxs-lookup"><span data-stu-id="e086e-416">To disable logons from all workstations to this account, set the UF\_ACCOUNTDISABLE in the **Flags** property of this class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e086e-417">Notes</span><span class="sxs-lookup"><span data-stu-id="e086e-417">Remarks</span></span>

<span data-ttu-id="e086e-418">La classe **Win32 \_ NetworkLoginProfile** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e086e-418">The **Win32\_NetworkLoginProfile** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="e086e-419">Le processus appelant qui utilise cette classe doit avoir le privilège **se \_ Restore \_ Name** sur l’ordinateur où se trouve le registre.</span><span class="sxs-lookup"><span data-stu-id="e086e-419">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="e086e-420">Pour plus d’informations, consultez [exécution d’opérations privilégiées](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="e086e-420">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e086e-421">Exemples</span><span class="sxs-lookup"><span data-stu-id="e086e-421">Examples</span></span>

<span data-ttu-id="e086e-422">L’exemple PowerShell [List login Network Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) retourne les informations de connexion réseau pour tous les utilisateurs d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e086e-422">The [List Network Login Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) PowerShell sample returns network login information for all the users of a computer.</span></span>

<span data-ttu-id="e086e-423">L’exemple VBScript suivant retourne les informations de connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="e086e-423">The following VBScript sample returns network login information.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
```



## <a name="requirements"></a><span data-ttu-id="e086e-424">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e086e-424">Requirements</span></span>



| <span data-ttu-id="e086e-425">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e086e-425">Requirement</span></span> | <span data-ttu-id="e086e-426">Valeur</span><span class="sxs-lookup"><span data-stu-id="e086e-426">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e086e-427">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e086e-427">Minimum supported client</span></span><br/> | <span data-ttu-id="e086e-428">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e086e-428">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e086e-429">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e086e-429">Minimum supported server</span></span><br/> | <span data-ttu-id="e086e-430">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e086e-430">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e086e-431">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e086e-431">Namespace</span></span><br/>                | <span data-ttu-id="e086e-432">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e086e-432">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e086e-433">MOF</span><span class="sxs-lookup"><span data-stu-id="e086e-433">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e086e-434"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e086e-434"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e086e-435">DLL</span><span class="sxs-lookup"><span data-stu-id="e086e-435">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e086e-436"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e086e-436"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e086e-437">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e086e-437">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e086e-438">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="e086e-438">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="e086e-439">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="e086e-439">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
