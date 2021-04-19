---
title: Structure WINBIO_STORAGE_SCHEMA ( \_ types WINBIO. h)
description: Décrit les fonctionnalités d’un adaptateur de stockage biométrique.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- API de Windows Biometric Framework de structure de WINBIO_STORAGE_SCHEMA
- API du pointeur de structure PWINBIO_STORAGE_SCHEMA Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28db23d55a7b3e43caaae5a88ca4bbf32fdf1178
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510364"
---
# <a name="winbio_storage_schema-structure"></a><span data-ttu-id="1b21b-105">Structure du schéma de \_ stockage WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="1b21b-105">WINBIO\_STORAGE\_SCHEMA structure</span></span>

<span data-ttu-id="1b21b-106">La structure du **\_ \_ schéma de stockage WINBIO** décrit les fonctionnalités d’un adaptateur de stockage biométrique.</span><span class="sxs-lookup"><span data-stu-id="1b21b-106">The **WINBIO\_STORAGE\_SCHEMA** structure describes the capabilities of a biometric storage adapter.</span></span> <span data-ttu-id="1b21b-107">Cette structure est utilisée par la fonction [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) .</span><span class="sxs-lookup"><span data-stu-id="1b21b-107">This structure is used by the [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b21b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b21b-108">Syntax</span></span>


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="1b21b-109">Membres</span><span class="sxs-lookup"><span data-stu-id="1b21b-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b21b-110">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="1b21b-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="1b21b-111">Type de mesure biométrique enregistrée dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="1b21b-111">The type of biometric measurement saved in the database.</span></span>

</dd> <dt>

<span data-ttu-id="1b21b-112">**DatabaseId**</span><span class="sxs-lookup"><span data-stu-id="1b21b-112">**DatabaseId**</span></span>
</dt> <dd>

<span data-ttu-id="1b21b-113">GUID qui identifie la base de données.</span><span class="sxs-lookup"><span data-stu-id="1b21b-113">A GUID that identifies the database.</span></span>

</dd> <dt>

<span data-ttu-id="1b21b-114">**DataFormat**</span><span class="sxs-lookup"><span data-stu-id="1b21b-114">**DataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="1b21b-115">GUID qui identifie le format des modèles dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="1b21b-115">A GUID that identifies the format of the templates in the database.</span></span>

</dd> <dt>

<span data-ttu-id="1b21b-116">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="1b21b-116">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="1b21b-117">Informations sur les caractéristiques de la base de données.</span><span class="sxs-lookup"><span data-stu-id="1b21b-117">Information about the characteristics of the database.</span></span> <span data-ttu-id="1b21b-118">Il peut s’agir d’une **opération or au niveau du** bit des constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b21b-118">This can be a bitwise **OR** of the following constants.</span></span>



| <span data-ttu-id="1b21b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b21b-119">Value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="1b21b-120">Signification</span><span class="sxs-lookup"><span data-stu-id="1b21b-120">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="1b21b-121"><dt>**WINBIO \_ \_ \_ Masque d’indicateur de base de données**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="1b21b-121"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="1b21b-122">Représente un masque pour les bits d’indicateur.</span><span class="sxs-lookup"><span data-stu-id="1b21b-122">Represents a mask for the flag bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="1b21b-123"><dt>**WINBIO \_ Indicateur de base de données 0x00020000 \_ \_ à distance**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1b21b-123"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="1b21b-124">La base de données se trouve sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="1b21b-124">The database resides on a remote computer.</span></span><br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="1b21b-125"><dt>**WINBIO \_ Indicateur de base de données 0x00010000 \_ \_ amovible**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1b21b-125"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="1b21b-126">La base de données réside sur un lecteur amovible.</span><span class="sxs-lookup"><span data-stu-id="1b21b-126">The database resides on a removable drive.</span></span><br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="1b21b-127"><dt>**WINBIO \_ TYPE de base de données \_ \_ SGBD**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="1b21b-127"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="1b21b-128">La base de données est gérée par un système de gestion de base de données.</span><span class="sxs-lookup"><span data-stu-id="1b21b-128">The database is managed by a database management system.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="1b21b-129"><dt>**WINBIO \_ \_ \_ Fichier de type base de données**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="1b21b-129"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="1b21b-130">La base de données est contenue dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="1b21b-130">The database is contained in a file.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="1b21b-131"><dt>**WINBIO \_ \_ \_ Masque de type de base de données**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="1b21b-131"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="1b21b-132">Représente un masque pour le type bits.</span><span class="sxs-lookup"><span data-stu-id="1b21b-132">Represents a mask for the type bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="1b21b-133"><dt>**WINBIO \_ TYPE de base de données \_ \_ ONCHIP**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="1b21b-133"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="1b21b-134">La base de données réside sur le capteur biométrique.</span><span class="sxs-lookup"><span data-stu-id="1b21b-134">The database resides on the biometric sensor.</span></span><br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="1b21b-135"><dt>**WINBIO \_ TYPE de base de données \_ \_ Smartcard**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="1b21b-135"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="1b21b-136">La base de données réside sur une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="1b21b-136">The database resides on a smart card.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="1b21b-137">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="1b21b-137">**FilePath**</span></span>
</dt> <dd>

<span data-ttu-id="1b21b-138">Le chemin d’accès et le nom de fichier de la base de données si elle réside sur le disque de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1b21b-138">The path and file name of the database if it resides on the computer disk.</span></span>

</dd> <dt>

<span data-ttu-id="1b21b-139">**ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="1b21b-139">**ConnectionString**</span></span>
</dt> <dd>

<span data-ttu-id="1b21b-140">Valeur de chaîne qui peut être envoyée à un serveur de base de données pour identifier la base de données.</span><span class="sxs-lookup"><span data-stu-id="1b21b-140">A string value that can be sent to a database server to identify the database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b21b-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b21b-141">Requirements</span></span>



| <span data-ttu-id="1b21b-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b21b-142">Requirement</span></span> | <span data-ttu-id="1b21b-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b21b-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b21b-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b21b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="1b21b-145">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b21b-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="1b21b-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b21b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="1b21b-147">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b21b-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1b21b-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b21b-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b21b-149"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b21b-149"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b21b-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b21b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b21b-151">Structures d’application cliente</span><span class="sxs-lookup"><span data-stu-id="1b21b-151">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="1b21b-152">**WinBioEnumDatabases**</span><span class="sxs-lookup"><span data-stu-id="1b21b-152">**WinBioEnumDatabases**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





