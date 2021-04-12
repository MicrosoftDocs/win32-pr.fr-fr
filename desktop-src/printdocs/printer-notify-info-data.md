---
description: La \_ structure de \_ \_ données d’informations de notification d’imprimante identifie un champ de travail ou d’informations sur l’imprimante et fournit les données actuelles pour ce champ.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: Structure PRINTER_NOTIFY_INFO_DATA (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203282"
---
# <a name="printer_notify_info_data-structure"></a><span data-ttu-id="1168d-103">\_Structure de \_ données d’informations de notification d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="1168d-103">PRINTER\_NOTIFY\_INFO\_DATA structure</span></span>

<span data-ttu-id="1168d-104">La structure de **\_ \_ \_ données** d’informations de notification d’imprimante identifie un champ de travail ou d’informations sur l’imprimante et fournit les données actuelles pour ce champ.</span><span class="sxs-lookup"><span data-stu-id="1168d-104">The **PRINTER\_NOTIFY\_INFO\_DATA** structure identifies a job or printer information field and provides the current data for that field.</span></span>

<span data-ttu-id="1168d-105">La fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) retourne une structure d' [**\_ \_ informations de notification d’imprimante**](printer-notify-info.md) , qui contient un tableau de structures de **\_ \_ \_ données d’informations de notification d’imprimante** .</span><span class="sxs-lookup"><span data-stu-id="1168d-105">The [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function returns a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of **PRINTER\_NOTIFY\_INFO\_DATA** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="1168d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1168d-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a><span data-ttu-id="1168d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1168d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1168d-108">**Type**</span><span class="sxs-lookup"><span data-stu-id="1168d-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="1168d-109">Indique le type d’informations fournies.</span><span class="sxs-lookup"><span data-stu-id="1168d-109">Indicates the type of information provided.</span></span> <span data-ttu-id="1168d-110">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1168d-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="1168d-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="1168d-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="1168d-112">Signification</span><span class="sxs-lookup"><span data-stu-id="1168d-112">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="1168d-113"><dt>**Travail \_ \_Type de notification**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="1168d-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="1168d-114">Indique que le membre **champ** spécifie une \_ constante de champ de notification de travail \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="1168d-114">Indicates that the **Field** member specifies a JOB\_NOTIFY\_FIELD\_\* constant.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="1168d-115"><dt>**Imprimante \_ \_Type de notification**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="1168d-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="1168d-116">Indique que le membre **champ** spécifie une \_ constante de champ de notification d’imprimante \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="1168d-116">Indicates that the **Field** member specifies a PRINTER\_NOTIFY\_FIELD\_\* constant.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1168d-117">**Champ**</span><span class="sxs-lookup"><span data-stu-id="1168d-117">**Field**</span></span>
</dt> <dd>

<span data-ttu-id="1168d-118">Indique le champ qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="1168d-118">Indicates the field that changed.</span></span> <span data-ttu-id="1168d-119">Pour obtenir la liste des valeurs possibles, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1168d-119">For a list of possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="1168d-120">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="1168d-120">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="1168d-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="1168d-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1168d-122">**Id**</span><span class="sxs-lookup"><span data-stu-id="1168d-122">**Id**</span></span>
</dt> <dd>

<span data-ttu-id="1168d-123">Indique l’identificateur du travail si le membre du **type** spécifie le type de notification du travail \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1168d-123">Indicates the job identifier if the **Type** member specifies JOB\_NOTIFY\_TYPE.</span></span> <span data-ttu-id="1168d-124">Si le membre de **type** spécifie le \_ type de notification d’imprimante \_ , ce membre n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="1168d-124">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="1168d-125">**NotifyData**</span><span class="sxs-lookup"><span data-stu-id="1168d-125">**NotifyData**</span></span>
</dt> <dd>

<span data-ttu-id="1168d-126">Union d’informations de données basées sur les membres du **type** et du **champ** .</span><span class="sxs-lookup"><span data-stu-id="1168d-126">A union of data information based on the **Type** and **Field** members.</span></span> <span data-ttu-id="1168d-127">Pour obtenir une description du type de données associé à chaque champ, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1168d-127">For a description of the type of data associated with each field, see the Remarks section.</span></span>

<dl> <dt>

<span data-ttu-id="1168d-128">**adwData \[ 2\]**</span><span class="sxs-lookup"><span data-stu-id="1168d-128">**adwData\[2\]**</span></span>
</dt> <dd>

<span data-ttu-id="1168d-129">Tableau de deux valeurs **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="1168d-129">An array of two **DWORD** values.</span></span> <span data-ttu-id="1168d-130">Pour les champs d’informations qui n’utilisent qu’une seule **valeur DWORD**, les données se trouvent dans **adwData** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="1168d-130">For information fields that use only a single **DWORD**, the data is in **adwData** \[0\].</span></span>

</dd> <dt>

<span data-ttu-id="1168d-131">**Données**</span><span class="sxs-lookup"><span data-stu-id="1168d-131">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1168d-132">**cbBuf**</span><span class="sxs-lookup"><span data-stu-id="1168d-132">**cbBuf**</span></span>
</dt> <dd>

<span data-ttu-id="1168d-133">Indique la taille, en octets, de la mémoire tampon vers laquelle pointe **pBuf**.</span><span class="sxs-lookup"><span data-stu-id="1168d-133">Indicates the size, in bytes, of the buffer pointed to by **pBuf**.</span></span>

</dd> <dt>

<span data-ttu-id="1168d-134">**pBuf**</span><span class="sxs-lookup"><span data-stu-id="1168d-134">**pBuf**</span></span>
</dt> <dd>

<span data-ttu-id="1168d-135">Pointeur vers une mémoire tampon qui contient les données actuelles du champ.</span><span class="sxs-lookup"><span data-stu-id="1168d-135">Pointer to a buffer that contains the field's current data.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1168d-136">Notes</span><span class="sxs-lookup"><span data-stu-id="1168d-136">Remarks</span></span>

<span data-ttu-id="1168d-137">Si le membre de **type** spécifie le \_ type de notification d’imprimante \_ , le membre de **champ** peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1168d-137">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1168d-138">Champ</span><span class="sxs-lookup"><span data-stu-id="1168d-138">Field</span></span></th>
<th><span data-ttu-id="1168d-139">Type de données</span><span class="sxs-lookup"><span data-stu-id="1168d-139">Type of data</span></span></th>
<th><span data-ttu-id="1168d-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="1168d-140">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1168d-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="1168d-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span></span></td>
<td><span data-ttu-id="1168d-142">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1168d-142">Not supported.</span></span></td>
<td><span data-ttu-id="1168d-143">0x00</span><span class="sxs-lookup"><span data-stu-id="1168d-143">0x00</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span><span class="sxs-lookup"><span data-stu-id="1168d-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span></span></td>
<td><span data-ttu-id="1168d-145"><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui contient le nom de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-145"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer.</span></span></td>
<td><span data-ttu-id="1168d-146">0x01</span><span class="sxs-lookup"><span data-stu-id="1168d-146">0x01</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span><span class="sxs-lookup"><span data-stu-id="1168d-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span></span></td>
<td><span data-ttu-id="1168d-148"><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui identifie le point de partage de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-148"><strong>pBuf</strong> is a pointer to a null-terminated string that identifies the share point for the printer.</span></span></td>
<td><span data-ttu-id="1168d-149">0x02</span><span class="sxs-lookup"><span data-stu-id="1168d-149">0x02</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span><span class="sxs-lookup"><span data-stu-id="1168d-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span></span></td>
<td><span data-ttu-id="1168d-151"><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui contient le nom du port sur lequel les travaux d’impression seront imprimés.</span><span class="sxs-lookup"><span data-stu-id="1168d-151"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the port that the print jobs will be printed to.</span></span> <span data-ttu-id="1168d-152">Si &quot; &quot; le regroupement d’imprimantes est sélectionné, il s’agit d’une liste de ports séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="1168d-152">If &quot;Printer Pooling&quot; is selected, this is a comma separated list of ports.</span></span></td>
<td><span data-ttu-id="1168d-153">0x03</span><span class="sxs-lookup"><span data-stu-id="1168d-153">0x03</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span><span class="sxs-lookup"><span data-stu-id="1168d-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span></span></td>
<td><span data-ttu-id="1168d-155"><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui contient le nom du pilote de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-155"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer's driver.</span></span></td>
<td><span data-ttu-id="1168d-156">0x04</span><span class="sxs-lookup"><span data-stu-id="1168d-156">0x04</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-157">PRINTER_NOTIFY_FIELD_COMMENT</span><span class="sxs-lookup"><span data-stu-id="1168d-157">PRINTER_NOTIFY_FIELD_COMMENT</span></span></td>
<td><span data-ttu-id="1168d-158"><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui contient la nouvelle chaîne de commentaire, qui est généralement une brève description de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-158"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new comment string, which is typically a brief description of the printer.</span></span></td>
<td><span data-ttu-id="1168d-159">0x05</span><span class="sxs-lookup"><span data-stu-id="1168d-159">0x05</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-160">PRINTER_NOTIFY_FIELD_LOCATION</span><span class="sxs-lookup"><span data-stu-id="1168d-160">PRINTER_NOTIFY_FIELD_LOCATION</span></span></td>
<td><span data-ttu-id="1168d-161"><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui contient le nouvel emplacement physique de l’imprimante (par exemple, &quot; Bldg.</span><span class="sxs-lookup"><span data-stu-id="1168d-161"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new physical location of the printer (for example, &quot;Bldg.</span></span> <span data-ttu-id="1168d-162">38, salle 1164 &quot; ).</span><span class="sxs-lookup"><span data-stu-id="1168d-162">38, Room 1164&quot;).</span></span></td>
<td><span data-ttu-id="1168d-163">0x06</span><span class="sxs-lookup"><span data-stu-id="1168d-163">0x06</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-164">PRINTER_NOTIFY_FIELD_DEVMODE</span><span class="sxs-lookup"><span data-stu-id="1168d-164">PRINTER_NOTIFY_FIELD_DEVMODE</span></span></td>
<td><span data-ttu-id="1168d-165"><strong>pBuf</strong> est un pointeur vers une structure <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> qui définit les données d’imprimante par défaut telles que l’orientation du papier et la résolution.</span><span class="sxs-lookup"><span data-stu-id="1168d-165"><strong>pBuf</strong> is a pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> structure that defines default printer data such as the paper orientation and the resolution.</span></span></td>
<td><span data-ttu-id="1168d-166">0x07</span><span class="sxs-lookup"><span data-stu-id="1168d-166">0x07</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-167">PRINTER_NOTIFY_FIELD_SEPFILE</span><span class="sxs-lookup"><span data-stu-id="1168d-167">PRINTER_NOTIFY_FIELD_SEPFILE</span></span></td>
<td><span data-ttu-id="1168d-168"><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fichier utilisé pour créer la page de séparation.</span><span class="sxs-lookup"><span data-stu-id="1168d-168"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="1168d-169">Cette page est utilisée pour séparer les travaux d’impression envoyés à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-169">This page is used to separate print jobs sent to the printer.</span></span></td>
<td><span data-ttu-id="1168d-170">0x08</span><span class="sxs-lookup"><span data-stu-id="1168d-170">0x08</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="1168d-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span></span></td>
<td><span data-ttu-id="1168d-172"><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur d’impression utilisé par l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-172"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span></td>
<td><span data-ttu-id="1168d-173">0x09</span><span class="sxs-lookup"><span data-stu-id="1168d-173">0x09</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1168d-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span></span></td>
<td><span data-ttu-id="1168d-175"><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui spécifie les paramètres du processeur d’impression par défaut.</span><span class="sxs-lookup"><span data-stu-id="1168d-175"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the default print-processor parameters.</span></span></td>
<td><span data-ttu-id="1168d-176">0x0A</span><span class="sxs-lookup"><span data-stu-id="1168d-176">0x0A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-177">PRINTER_NOTIFY_FIELD_DATATYPE</span><span class="sxs-lookup"><span data-stu-id="1168d-177">PRINTER_NOTIFY_FIELD_DATATYPE</span></span></td>
<td><span data-ttu-id="1168d-178"><strong>pBuf</strong> est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données utilisé pour enregistrer le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="1168d-178"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the data type used to record the print job.</span></span></td>
<td><span data-ttu-id="1168d-179">0x0B</span><span class="sxs-lookup"><span data-stu-id="1168d-179">0x0B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span><span class="sxs-lookup"><span data-stu-id="1168d-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span></span></td>
<td><span data-ttu-id="1168d-181"><strong>pBuf</strong> est un pointeur vers une structure <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-181"><strong>pBuf</strong> is a pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> structure for the printer.</span></span> <span data-ttu-id="1168d-182">Le pointeur peut être <strong>null</strong> s’il n’existe aucun descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1168d-182">The pointer may be <strong>NULL</strong> if there is no security descriptor.</span></span></td>
<td><span data-ttu-id="1168d-183">0x0C</span><span class="sxs-lookup"><span data-stu-id="1168d-183">0x0C</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="1168d-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span></span></td>
<td><span data-ttu-id="1168d-185"><strong>adwData</strong> [0] spécifie les attributs d’imprimante, qui peuvent être l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1168d-185"><strong>adwData</strong> [0] specifies the printer attributes, which can be one of the following values:</span></span><dl> <span data-ttu-id="1168d-186">PRINTER_ATTRIBUTE_QUEUED</span><span class="sxs-lookup"><span data-stu-id="1168d-186">PRINTER_ATTRIBUTE_QUEUED</span></span><br />
<span data-ttu-id="1168d-187">PRINTER_ATTRIBUTE_DIRECT</span><span class="sxs-lookup"><span data-stu-id="1168d-187">PRINTER_ATTRIBUTE_DIRECT</span></span><br />
<span data-ttu-id="1168d-188">PRINTER_ATTRIBUTE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="1168d-188">PRINTER_ATTRIBUTE_DEFAULT</span></span><br />
<span data-ttu-id="1168d-189">PRINTER_ATTRIBUTE_SHARED</span><span class="sxs-lookup"><span data-stu-id="1168d-189">PRINTER_ATTRIBUTE_SHARED</span></span><br />
</dl></td>
<td><span data-ttu-id="1168d-190">0x0D</span><span class="sxs-lookup"><span data-stu-id="1168d-190">0x0D</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-191">PRINTER_NOTIFY_FIELD_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="1168d-191">PRINTER_NOTIFY_FIELD_PRIORITY</span></span></td>
<td><span data-ttu-id="1168d-192"><strong>adwData</strong> [0] spécifie une valeur de priorité que le spouleur utilise pour router les travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="1168d-192"><strong>adwData</strong> [0] specifies a priority value that the spooler uses to route print jobs.</span></span></td>
<td><span data-ttu-id="1168d-193">0x0E</span><span class="sxs-lookup"><span data-stu-id="1168d-193">0x0E</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="1168d-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span></span></td>
<td><span data-ttu-id="1168d-195"><strong>adwData</strong> [0] spécifie la valeur de priorité par défaut affectée à chaque travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="1168d-195"><strong>adwData</strong> [0] specifies the default priority value assigned to each print job.</span></span></td>
<td><span data-ttu-id="1168d-196">0x0F</span><span class="sxs-lookup"><span data-stu-id="1168d-196">0x0F</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-197">PRINTER_NOTIFY_FIELD_START_TIME</span><span class="sxs-lookup"><span data-stu-id="1168d-197">PRINTER_NOTIFY_FIELD_START_TIME</span></span></td>
<td><span data-ttu-id="1168d-198"><strong>adwData</strong> [0] spécifie l’heure la plus ancienne à laquelle l’imprimante imprime un travail.</span><span class="sxs-lookup"><span data-stu-id="1168d-198"><strong>adwData</strong> [0] specifies the earliest time at which the printer will print a job.</span></span> <span data-ttu-id="1168d-199">(Cette valeur est spécifiée en minutes écoulées depuis 12:00 heures)</span><span class="sxs-lookup"><span data-stu-id="1168d-199">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="1168d-200">0x10</span><span class="sxs-lookup"><span data-stu-id="1168d-200">0x10</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span><span class="sxs-lookup"><span data-stu-id="1168d-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span></span></td>
<td><span data-ttu-id="1168d-202"><strong>adwData</strong> [0] spécifie l’heure la plus récente à laquelle l’imprimante imprime un travail.</span><span class="sxs-lookup"><span data-stu-id="1168d-202"><strong>adwData</strong> [0] specifies the latest time at which the printer will print a job.</span></span> <span data-ttu-id="1168d-203">(Cette valeur est spécifiée en minutes écoulées depuis 12:00 heures)</span><span class="sxs-lookup"><span data-stu-id="1168d-203">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="1168d-204">0x11</span><span class="sxs-lookup"><span data-stu-id="1168d-204">0x11</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-205">PRINTER_NOTIFY_FIELD_STATUS</span><span class="sxs-lookup"><span data-stu-id="1168d-205">PRINTER_NOTIFY_FIELD_STATUS</span></span></td>
<td><span data-ttu-id="1168d-206"><strong>adwData</strong> [0] spécifie l’état de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-206"><strong>adwData</strong> [0] specifies the printer status.</span></span> <span data-ttu-id="1168d-207">Pour obtenir la liste des valeurs possibles, consultez la structure <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1168d-207">For a list of possible values, see the <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> structure.</span></span></td>
<td><span data-ttu-id="1168d-208">0x12</span><span class="sxs-lookup"><span data-stu-id="1168d-208">0x12</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span><span class="sxs-lookup"><span data-stu-id="1168d-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span></span></td>
<td><span data-ttu-id="1168d-210">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1168d-210">Not supported.</span></span></td>
<td><span data-ttu-id="1168d-211">0x13</span><span class="sxs-lookup"><span data-stu-id="1168d-211">0x13</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-212">PRINTER_NOTIFY_FIELD_CJOBS</span><span class="sxs-lookup"><span data-stu-id="1168d-212">PRINTER_NOTIFY_FIELD_CJOBS</span></span></td>
<td><span data-ttu-id="1168d-213"><strong>adwData</strong> [0] spécifie le nombre de travaux d’impression qui ont été mis en file d’attente pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-213"><strong>adwData</strong> [0] specifies the number of print jobs that have been queued for the printer.</span></span></td>
<td><span data-ttu-id="1168d-214">0x14</span><span class="sxs-lookup"><span data-stu-id="1168d-214">0x14</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span><span class="sxs-lookup"><span data-stu-id="1168d-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span></span></td>
<td><span data-ttu-id="1168d-216"><strong>adwData</strong> [0] spécifie le nombre moyen de pages par minute qui ont été imprimées sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-216"><strong>adwData</strong> [0] specifies the average number of pages per minute that have been printed on the printer.</span></span></td>
<td><span data-ttu-id="1168d-217">0x15</span><span class="sxs-lookup"><span data-stu-id="1168d-217">0x15</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span><span class="sxs-lookup"><span data-stu-id="1168d-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span></span></td>
<td><span data-ttu-id="1168d-219">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1168d-219">Not supported.</span></span></td>
<td><span data-ttu-id="1168d-220">0x16</span><span class="sxs-lookup"><span data-stu-id="1168d-220">0x16</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="1168d-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span></span></td>
<td><span data-ttu-id="1168d-222">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1168d-222">Not supported.</span></span></td>
<td><span data-ttu-id="1168d-223">0x17</span><span class="sxs-lookup"><span data-stu-id="1168d-223">0x17</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span><span class="sxs-lookup"><span data-stu-id="1168d-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span></span></td>
<td><span data-ttu-id="1168d-225">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1168d-225">Not supported.</span></span></td>
<td><span data-ttu-id="1168d-226">0x18</span><span class="sxs-lookup"><span data-stu-id="1168d-226">0x18</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="1168d-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span></span></td>
<td><span data-ttu-id="1168d-228">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1168d-228">Not supported.</span></span></td>
<td><span data-ttu-id="1168d-229">0x19</span><span class="sxs-lookup"><span data-stu-id="1168d-229">0x19</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1168d-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span><span class="sxs-lookup"><span data-stu-id="1168d-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span></span></td>
<td><span data-ttu-id="1168d-231">Cette valeur est définie si le GUID de l’objet change.</span><span class="sxs-lookup"><span data-stu-id="1168d-231">This is set if the object GUID changes.</span></span></td>
<td><span data-ttu-id="1168d-232">0x1A</span><span class="sxs-lookup"><span data-stu-id="1168d-232">0x1A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1168d-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="1168d-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span></span></td>
<td><span data-ttu-id="1168d-234">Cette valeur est définie si la connexion à l’imprimante est renommée.</span><span class="sxs-lookup"><span data-stu-id="1168d-234">This is set if the printer connection is renamed.</span></span></td>
<td><span data-ttu-id="1168d-235">0x1B</span><span class="sxs-lookup"><span data-stu-id="1168d-235">0x1B</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1168d-236">Si le membre de **type** spécifie le \_ type de notification de travail \_ , le membre de **champ** peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1168d-236">If the **Type** member specifies JOB\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



| <span data-ttu-id="1168d-237">Champ</span><span class="sxs-lookup"><span data-stu-id="1168d-237">Field</span></span>                                    | <span data-ttu-id="1168d-238">Type de données</span><span class="sxs-lookup"><span data-stu-id="1168d-238">Type of data</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="1168d-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="1168d-239">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="1168d-240">nom de l’imprimante du champ de \_ notification du travail \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="1168d-240">JOB\_NOTIFY\_FIELD\_PRINTER\_NAME</span></span>        | <span data-ttu-id="1168d-241">**pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui contient le nom de l’imprimante pour laquelle la tâche est mise en attente.</span><span class="sxs-lookup"><span data-stu-id="1168d-241">**pBuf** is a pointer to a null-terminated string containing the name of the printer for which the job is spooled.</span></span>                                                                                                                                      | <span data-ttu-id="1168d-242">0x00</span><span class="sxs-lookup"><span data-stu-id="1168d-242">0x00</span></span>  |
| <span data-ttu-id="1168d-243">\_nom d' \_ ordinateur du champ de notification du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="1168d-243">JOB\_NOTIFY\_FIELD\_MACHINE\_NAME</span></span>        | <span data-ttu-id="1168d-244">**pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’ordinateur qui a créé le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="1168d-244">**pBuf** is a pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>                                                                                                                                    | <span data-ttu-id="1168d-245">0x01</span><span class="sxs-lookup"><span data-stu-id="1168d-245">0x01</span></span>  |
| <span data-ttu-id="1168d-246">\_nom du \_ port du champ de notification du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="1168d-246">JOB\_NOTIFY\_FIELD\_PORT\_NAME</span></span>           | <span data-ttu-id="1168d-247">**pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui identifie le ou les ports utilisés pour transmettre des données à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-247">**pBuf** is a pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="1168d-248">Si une imprimante est connectée à plusieurs ports, les noms des ports sont séparés par des virgules (par exemple, « LPT1 :, LPT2 :, LPT3 : »).</span><span class="sxs-lookup"><span data-stu-id="1168d-248">If a printer is connected to more than one port, the names of the ports are separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span> | <span data-ttu-id="1168d-249">0x02</span><span class="sxs-lookup"><span data-stu-id="1168d-249">0x02</span></span>  |
| <span data-ttu-id="1168d-250">\_nom d' \_ utilisateur du champ de notification du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="1168d-250">JOB\_NOTIFY\_FIELD\_USER\_NAME</span></span>           | <span data-ttu-id="1168d-251">**pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’utilisateur qui a envoyé le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="1168d-251">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who sent the print job.</span></span>                                                                                                                                           | <span data-ttu-id="1168d-252">0x03</span><span class="sxs-lookup"><span data-stu-id="1168d-252">0x03</span></span>  |
| <span data-ttu-id="1168d-253">\_nom du \_ champ \_ NOTIFIer le travail \_</span><span class="sxs-lookup"><span data-stu-id="1168d-253">JOB\_NOTIFY\_FIELD\_NOTIFY\_NAME</span></span>         | <span data-ttu-id="1168d-254">**pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’utilisateur qui doit être averti lorsque le travail a été imprimé ou lorsqu’une erreur se produit lors de l’impression du travail.</span><span class="sxs-lookup"><span data-stu-id="1168d-254">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</span></span>                                                              | <span data-ttu-id="1168d-255">0x04</span><span class="sxs-lookup"><span data-stu-id="1168d-255">0x04</span></span>  |
| <span data-ttu-id="1168d-256">\_type de \_ données du champ de notification du travail \_</span><span class="sxs-lookup"><span data-stu-id="1168d-256">JOB\_NOTIFY\_FIELD\_DATATYPE</span></span>             | <span data-ttu-id="1168d-257">**pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données utilisé pour enregistrer le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="1168d-257">**pBuf** is a pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>                                                                                                                                         | <span data-ttu-id="1168d-258">0x05</span><span class="sxs-lookup"><span data-stu-id="1168d-258">0x05</span></span>  |
| <span data-ttu-id="1168d-259">\_processeur d' \_ impression du champ de notification du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="1168d-259">JOB\_NOTIFY\_FIELD\_PRINT\_PROCESSOR</span></span>     | <span data-ttu-id="1168d-260">**pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur d’impression à utiliser pour imprimer le travail.</span><span class="sxs-lookup"><span data-stu-id="1168d-260">**pBuf** is a pointer to a null-terminated string that specifies the name of the print processor to be used to print the job.</span></span>                                                                                                                           | <span data-ttu-id="1168d-261">0x06</span><span class="sxs-lookup"><span data-stu-id="1168d-261">0x06</span></span>  |
| <span data-ttu-id="1168d-262">\_paramètres du \_ champ de notification du travail \_</span><span class="sxs-lookup"><span data-stu-id="1168d-262">JOB\_NOTIFY\_FIELD\_PARAMETERS</span></span>           | <span data-ttu-id="1168d-263">**pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie les paramètres du processeur d’impression.</span><span class="sxs-lookup"><span data-stu-id="1168d-263">**pBuf** is a pointer to a null-terminated string that specifies print-processor parameters.</span></span>                                                                                                                                                            | <span data-ttu-id="1168d-264">0x07</span><span class="sxs-lookup"><span data-stu-id="1168d-264">0x07</span></span>  |
| <span data-ttu-id="1168d-265">\_nom du \_ pilote du champ de notification du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="1168d-265">JOB\_NOTIFY\_FIELD\_DRIVER\_NAME</span></span>         | <span data-ttu-id="1168d-266">**pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote d’imprimante qui doit être utilisé pour traiter le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="1168d-266">**pBuf** is a pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>                                                                                                           | <span data-ttu-id="1168d-267">0x08</span><span class="sxs-lookup"><span data-stu-id="1168d-267">0x08</span></span>  |
| <span data-ttu-id="1168d-268">champ de notification de tâche \_ \_ \_ DEVMODE</span><span class="sxs-lookup"><span data-stu-id="1168d-268">JOB\_NOTIFY\_FIELD\_DEVMODE</span></span>              | <span data-ttu-id="1168d-269">**pBuf** est un pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui contient des données d’initialisation d’appareil et d’environnement pour le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-269">**pBuf** is a pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>                                                                                                        | <span data-ttu-id="1168d-270">0x09</span><span class="sxs-lookup"><span data-stu-id="1168d-270">0x09</span></span>  |
| <span data-ttu-id="1168d-271">\_État du \_ champ de notification du travail \_</span><span class="sxs-lookup"><span data-stu-id="1168d-271">JOB\_NOTIFY\_FIELD\_STATUS</span></span>               | <span data-ttu-id="1168d-272">**adwData** \[ 0 \] spécifie l’état du travail.</span><span class="sxs-lookup"><span data-stu-id="1168d-272">**adwData** \[0\] specifies the job status.</span></span> <span data-ttu-id="1168d-273">Pour obtenir la liste des valeurs possibles, consultez la structure [**Job \_ info \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="1168d-273">For a list of possible values, see the [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>                                                                                                                        | <span data-ttu-id="1168d-274">0x0A</span><span class="sxs-lookup"><span data-stu-id="1168d-274">0x0A</span></span>  |
| <span data-ttu-id="1168d-275">\_chaîne d' \_ État du champ de notification du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="1168d-275">JOB\_NOTIFY\_FIELD\_STATUS\_STRING</span></span>       | <span data-ttu-id="1168d-276">**pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie l’état du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="1168d-276">**pBuf** is a pointer to a null-terminated string that specifies the status of the print job.</span></span>                                                                                                                                                           | <span data-ttu-id="1168d-277">0x0B</span><span class="sxs-lookup"><span data-stu-id="1168d-277">0x0B</span></span>  |
| <span data-ttu-id="1168d-278">\_descripteur de sécurité de champ de notification de travail \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="1168d-278">JOB\_NOTIFY\_FIELD\_SECURITY\_DESCRIPTOR</span></span> | <span data-ttu-id="1168d-279">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1168d-279">Not supported.</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="1168d-280">0x0C</span><span class="sxs-lookup"><span data-stu-id="1168d-280">0x0C</span></span>  |
| <span data-ttu-id="1168d-281">\_document de \_ champ de notification de tâche \_</span><span class="sxs-lookup"><span data-stu-id="1168d-281">JOB\_NOTIFY\_FIELD\_DOCUMENT</span></span>             | <span data-ttu-id="1168d-282">**pBuf** est un pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du travail d’impression (par exemple, « MS-WORD : Review.doc »).</span><span class="sxs-lookup"><span data-stu-id="1168d-282">**pBuf** is a pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>                                                                                                                        | <span data-ttu-id="1168d-283">0x0D</span><span class="sxs-lookup"><span data-stu-id="1168d-283">0x0D</span></span>  |
| <span data-ttu-id="1168d-284">\_priorité du \_ champ de notification du travail \_</span><span class="sxs-lookup"><span data-stu-id="1168d-284">JOB\_NOTIFY\_FIELD\_PRIORITY</span></span>             | <span data-ttu-id="1168d-285">**adwData** \[ 0 \] spécifie la priorité du travail.</span><span class="sxs-lookup"><span data-stu-id="1168d-285">**adwData** \[0\] specifies the job priority.</span></span>                                                                                                                                                                                                           | <span data-ttu-id="1168d-286">0x0E</span><span class="sxs-lookup"><span data-stu-id="1168d-286">0x0E</span></span>  |
| <span data-ttu-id="1168d-287">\_position du \_ champ de notification du travail \_</span><span class="sxs-lookup"><span data-stu-id="1168d-287">JOB\_NOTIFY\_FIELD\_POSITION</span></span>             | <span data-ttu-id="1168d-288">**adwData** \[ 0 \] spécifie la position du travail dans la file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="1168d-288">**adwData** \[0\] specifies the job's position in the print queue.</span></span>                                                                                                                                                                                      | <span data-ttu-id="1168d-289">0x0F</span><span class="sxs-lookup"><span data-stu-id="1168d-289">0x0F</span></span>  |
| <span data-ttu-id="1168d-290">champ de notification de travail \_ \_ \_ envoyé</span><span class="sxs-lookup"><span data-stu-id="1168d-290">JOB\_NOTIFY\_FIELD\_SUBMITTED</span></span>            | <span data-ttu-id="1168d-291">**pBuf** est un pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui spécifie l’heure à laquelle le travail a été soumis.</span><span class="sxs-lookup"><span data-stu-id="1168d-291">**pBuf** is a pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>                                                                                                                          | <span data-ttu-id="1168d-292">0x10</span><span class="sxs-lookup"><span data-stu-id="1168d-292">0x10</span></span>  |
| <span data-ttu-id="1168d-293">\_heure de \_ début du champ de notification du travail \_ \_</span><span class="sxs-lookup"><span data-stu-id="1168d-293">JOB\_NOTIFY\_FIELD\_START\_TIME</span></span>          | <span data-ttu-id="1168d-294">**adwData** \[ 0 \] spécifie l’heure à laquelle le travail peut être imprimé au plus tôt.</span><span class="sxs-lookup"><span data-stu-id="1168d-294">**adwData** \[0\] specifies the earliest time that the job can be printed.</span></span> <span data-ttu-id="1168d-295">(Cette valeur est spécifiée en minutes écoulées depuis 12:00 heures)</span><span class="sxs-lookup"><span data-stu-id="1168d-295">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                | <span data-ttu-id="1168d-296">0x11</span><span class="sxs-lookup"><span data-stu-id="1168d-296">0x11</span></span>  |
| <span data-ttu-id="1168d-297">champ de notification du travail \_ \_ \_ jusqu’à l' \_ heure</span><span class="sxs-lookup"><span data-stu-id="1168d-297">JOB\_NOTIFY\_FIELD\_UNTIL\_TIME</span></span>          | <span data-ttu-id="1168d-298">**adwData** \[ 0 \] spécifie l’heure à laquelle le travail peut être imprimé au plus tard.</span><span class="sxs-lookup"><span data-stu-id="1168d-298">**adwData** \[0\] specifies the latest time that the job can be printed.</span></span> <span data-ttu-id="1168d-299">(Cette valeur est spécifiée en minutes écoulées depuis 12:00 heures)</span><span class="sxs-lookup"><span data-stu-id="1168d-299">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                  | <span data-ttu-id="1168d-300">0x12</span><span class="sxs-lookup"><span data-stu-id="1168d-300">0x12</span></span>  |
| <span data-ttu-id="1168d-301">\_heure du \_ champ de notification du travail \_</span><span class="sxs-lookup"><span data-stu-id="1168d-301">JOB\_NOTIFY\_FIELD\_TIME</span></span>                 | <span data-ttu-id="1168d-302">**adwData** \[ 0 \] spécifie la durée totale, en secondes, qui s’est écoulée depuis le début de l’impression du travail.</span><span class="sxs-lookup"><span data-stu-id="1168d-302">**adwData** \[0\] specifies the total time, in seconds, that has elapsed since the job began printing.</span></span>                                                                                                                                                  | <span data-ttu-id="1168d-303">0x13</span><span class="sxs-lookup"><span data-stu-id="1168d-303">0x13</span></span>  |
| <span data-ttu-id="1168d-304">\_ \_ \_ nombre total de \_ pages du champ notifier le travail</span><span class="sxs-lookup"><span data-stu-id="1168d-304">JOB\_NOTIFY\_FIELD\_TOTAL\_PAGES</span></span>         | <span data-ttu-id="1168d-305">**adwData** \[ 0 \] spécifie la taille, en pages, du travail.</span><span class="sxs-lookup"><span data-stu-id="1168d-305">**adwData** \[0\] specifies the size, in pages, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="1168d-306">0x14</span><span class="sxs-lookup"><span data-stu-id="1168d-306">0x14</span></span>  |
| <span data-ttu-id="1168d-307">PAGES de champs de notification de travail \_ \_ \_ \_ imprimées</span><span class="sxs-lookup"><span data-stu-id="1168d-307">JOB\_NOTIFY\_FIELD\_PAGES\_PRINTED</span></span>       | <span data-ttu-id="1168d-308">**adwData** \[ 0 \] spécifie le nombre de pages qui ont été imprimées.</span><span class="sxs-lookup"><span data-stu-id="1168d-308">**adwData** \[0\] specifies the number of pages that have printed.</span></span>                                                                                                                                                                                      | <span data-ttu-id="1168d-309">0x15</span><span class="sxs-lookup"><span data-stu-id="1168d-309">0x15</span></span>  |
| <span data-ttu-id="1168d-310">champ de notification du travail- \_ \_ \_ nombre total d' \_ octets</span><span class="sxs-lookup"><span data-stu-id="1168d-310">JOB\_NOTIFY\_FIELD\_TOTAL\_BYTES</span></span>         | <span data-ttu-id="1168d-311">**adwData** \[ 0 \] spécifie la taille, en octets, du travail.</span><span class="sxs-lookup"><span data-stu-id="1168d-311">**adwData** \[0\] specifies the size, in bytes, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="1168d-312">0x16</span><span class="sxs-lookup"><span data-stu-id="1168d-312">0x16</span></span>  |
| <span data-ttu-id="1168d-313">octets du champ de notification du travail \_ \_ \_ \_ imprimés</span><span class="sxs-lookup"><span data-stu-id="1168d-313">JOB\_NOTIFY\_FIELD\_BYTES\_PRINTED</span></span>       | <span data-ttu-id="1168d-314">**adwData** \[ 0 \] spécifie le nombre d’octets qui ont été imprimés sur ce travail.</span><span class="sxs-lookup"><span data-stu-id="1168d-314">**adwData** \[0\] specifies the number of bytes that have been printed on this job.</span></span> <span data-ttu-id="1168d-315">Pour ce champ, l’objet de notification de modification est signalé lorsque des octets sont envoyés à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="1168d-315">For this field, the change notification object is signaled when bytes are sent to the printer.</span></span>                                                                      | <span data-ttu-id="1168d-316">0x17</span><span class="sxs-lookup"><span data-stu-id="1168d-316">0x17</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="1168d-317">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1168d-317">Requirements</span></span>



| <span data-ttu-id="1168d-318">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1168d-318">Requirement</span></span> | <span data-ttu-id="1168d-319">Valeur</span><span class="sxs-lookup"><span data-stu-id="1168d-319">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1168d-320">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1168d-320">Minimum supported client</span></span><br/> | <span data-ttu-id="1168d-321">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1168d-321">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1168d-322">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1168d-322">Minimum supported server</span></span><br/> | <span data-ttu-id="1168d-323">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1168d-323">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1168d-324">En-tête</span><span class="sxs-lookup"><span data-stu-id="1168d-324">Header</span></span><br/>                   | <dl> <span data-ttu-id="1168d-325"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1168d-325"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1168d-326">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1168d-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1168d-327">Impression</span><span class="sxs-lookup"><span data-stu-id="1168d-327">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1168d-328">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="1168d-328">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="1168d-329">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="1168d-329">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="1168d-330">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="1168d-330">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="1168d-331">**\_Informations sur le travail \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1168d-331">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="1168d-332">**\_Infos sur l’imprimante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1168d-332">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="1168d-333">**\_informations de notification de l’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="1168d-333">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="1168d-334">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="1168d-334">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="1168d-335">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="1168d-335">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

