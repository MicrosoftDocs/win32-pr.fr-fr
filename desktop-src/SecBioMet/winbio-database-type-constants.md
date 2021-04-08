---
title: Constantes WINBIO_DATABASE_TYPE ( \_ types WINBIO. h)
description: Indicateurs qui peuvent être utilisés pour le membre Attributes de la \_ structure de schéma de stockage WINBIO \_ .
ms.assetid: 07e7e91c-3ca6-41cd-a2c7-ac43bb5156a6
topic_type:
- apiref
api_name:
- WINBIO_DATABASE_TYPE_MASK
- WINBIO_DATABASE_TYPE_FILE
- WINBIO_DATABASE_TYPE_DBMS
- WINBIO_DATABASE_TYPE_ONCHIP
- WINBIO_DATABASE_TYPE_SMARTCARD
- WINBIO_DATABASE_FLAG_MASK
- WINBIO_DATABASE_FLAG_REMOVABLE
- WINBIO_DATABASE_FLAG_REMOTE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd67f49c5fa689fb4418789aae7c4d6c9a305a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741525"
---
# <a name="winbio_database_type-constants"></a><span data-ttu-id="91ac9-103">\_Constantes de type de base de données WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="91ac9-103">WINBIO\_DATABASE\_TYPE Constants</span></span>

<span data-ttu-id="91ac9-104">Les indicateurs suivants peuvent être utilisés pour le membre **attributes** de la structure de [**\_ \_ schéma de stockage WINBIO**](winbio-storage-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="91ac9-104">The following flags can be used for the **Attributes** member of the [**WINBIO\_STORAGE\_SCHEMA**](winbio-storage-schema.md) structure.</span></span>



| <span data-ttu-id="91ac9-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="91ac9-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="91ac9-106">Description</span><span class="sxs-lookup"><span data-stu-id="91ac9-106">Description</span></span>                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="91ac9-107"><dt>**WINBIO \_ \_ \_ Masque de type de base de données**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="91ac9-107"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="91ac9-108">Représente un masque pour tous les \_ bits de type \_ .</span><span class="sxs-lookup"><span data-stu-id="91ac9-108">Represents a mask for all of the \_TYPE\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="91ac9-109"><dt>**WINBIO \_ \_ \_ Fichier de type base de données**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="91ac9-109"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="91ac9-110">La base de données est contenue dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="91ac9-110">The database is contained in a file.</span></span><br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="91ac9-111"><dt>**WINBIO \_ TYPE de base de données \_ \_ SGBD**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="91ac9-111"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="91ac9-112">La base de données est gérée par un composant de système de gestion de base de données externe (SGBD), tel que Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="91ac9-112">The database is managed by an external database management system (DBMS) component, such as Microsoft SQL Server.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="91ac9-113"><dt>**WINBIO \_ TYPE de base de données \_ \_ ONCHIP**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="91ac9-113"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="91ac9-114">La base de données réside sur le capteur biométrique.</span><span class="sxs-lookup"><span data-stu-id="91ac9-114">The database resides on the biometric sensor.</span></span><br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="91ac9-115"><dt>**WINBIO \_ TYPE de base de données \_ \_ Smartcard**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="91ac9-115"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="91ac9-116">La base de données réside sur une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="91ac9-116">The database resides on a smart card.</span></span><br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="91ac9-117"><dt>**WINBIO \_ \_ \_ Masque d’indicateur de base de données**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="91ac9-117"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="91ac9-118">Représente un masque pour tous les \_ bits d’indicateur \_ .</span><span class="sxs-lookup"><span data-stu-id="91ac9-118">Represents a mask for all of the \_FLAG\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="91ac9-119"><dt>**WINBIO \_ Indicateur de base de données 0x00010000 \_ \_ amovible**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91ac9-119"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="91ac9-120">Le support de stockage contenant la base de données peut être physiquement supprimé de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="91ac9-120">The storage medium containing the database can be physically removed from the computer.</span></span><br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="91ac9-121"><dt>**WINBIO \_ Indicateur de base de données 0x00020000 \_ \_ à distance**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91ac9-121"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="91ac9-122">La base de données se trouve sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="91ac9-122">The database resides on a remote computer.</span></span><br/>                                                                        |



## <a name="requirements"></a><span data-ttu-id="91ac9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91ac9-123">Requirements</span></span>



| <span data-ttu-id="91ac9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91ac9-124">Requirement</span></span> | <span data-ttu-id="91ac9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="91ac9-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ac9-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91ac9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="91ac9-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91ac9-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="91ac9-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91ac9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="91ac9-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91ac9-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="91ac9-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="91ac9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="91ac9-131"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91ac9-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91ac9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91ac9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ac9-133">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="91ac9-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





