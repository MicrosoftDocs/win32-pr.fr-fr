---
description: Retourne l’opération de présence physique TPM en attente. Utilisez la méthode SetPhysicalPresenceRequest pour demander une opération.
ms.assetid: c50378ae-b465-4c82-beb9-8ecb7939dae2
title: Méthode GetPhysicalPresenceRequest de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8d631aabfc1e2df15aa4182b8332091fe503f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543523"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a><span data-ttu-id="b7937-104">Méthode GetPhysicalPresenceRequest de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="b7937-104">GetPhysicalPresenceRequest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="b7937-105">La méthode **GetPhysicalPresenceRequest** de la [**classe \_ TPM Win32**](win32-tpm.md) retourne l’opération de présence physique TPM en attente.</span><span class="sxs-lookup"><span data-stu-id="b7937-105">The **GetPhysicalPresenceRequest** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="b7937-106">Utilisez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) pour demander une opération.</span><span class="sxs-lookup"><span data-stu-id="b7937-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7937-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7937-107">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a><span data-ttu-id="b7937-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7937-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7937-109">*Demande* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b7937-109">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7937-110">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7937-110">Type: **uint32**</span></span>

<span data-ttu-id="b7937-111">Valeur qui spécifie l’opération de présence physique TPM en attente.</span><span class="sxs-lookup"><span data-stu-id="b7937-111">A value that specifies the pending TPM physical presence operation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7937-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7937-112">Value</span></span></th>
<th><span data-ttu-id="b7937-113">Signification</span><span class="sxs-lookup"><span data-stu-id="b7937-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="b7937-114"><dt>entre</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-114"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-115">Aucune demande.</span><span class="sxs-lookup"><span data-stu-id="b7937-115">No request.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b7937-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-117">Activez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-117">Enable the TPM.</span></span><br/> <span data-ttu-id="b7937-118">Cette opération est inversée par l’opération 2.</span><span class="sxs-lookup"><span data-stu-id="b7937-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="b7937-119">Pour plus d’informations, consultez les méthodes associées qui n’impliquent pas de présence physique :</span><span class="sxs-lookup"><span data-stu-id="b7937-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="b7937-120"><a href="enable-win32-tpm.md"><strong>Activer</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7937-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="b7937-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7937-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b7937-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-123">Désactivez le module TPM.</span><span class="sxs-lookup"><span data-stu-id="b7937-123">Disable the TPM.</span></span><br/> <span data-ttu-id="b7937-124">Cette opération est inversée par l’opération 1.</span><span class="sxs-lookup"><span data-stu-id="b7937-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="b7937-125">Pour plus d’informations, consultez cette méthode associée qui n’implique pas de présence physique : <a href="disable-win32-tpm.md"><strong>Désactiver</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b7937-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b7937-126"><dt>1,3</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-127">Activez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-127">Activate the TPM.</span></span><br/> <span data-ttu-id="b7937-128">Cette opération est inversée par l’opération 4.</span><span class="sxs-lookup"><span data-stu-id="b7937-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b7937-129"><dt>4</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-130">Désactivez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="b7937-131">Cette opération est inversée par l’opération 3.</span><span class="sxs-lookup"><span data-stu-id="b7937-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b7937-132"><dt>5,5</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-133">Effacez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-133">Clear the TPM.</span></span><br/> <span data-ttu-id="b7937-134">Cette opération ne peut pas être inversée.</span><span class="sxs-lookup"><span data-stu-id="b7937-134">This operation cannot be reversed.</span></span><br/> <span data-ttu-id="b7937-135">Pour plus d’informations, consultez cette méthode associée qui n’implique pas la présence physique : <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b7937-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b7937-136"><dt>6,3</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-137">Activez et activez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-137">Enable and activate the TPM.</span></span> <br/> <span data-ttu-id="b7937-138">Cette opération est inversée par l’opération 7.</span><span class="sxs-lookup"><span data-stu-id="b7937-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b7937-139"><dt>Commission(7</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-140">Désactivez et désactivez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="b7937-141">Cette opération est inversée par l’opération 6.</span><span class="sxs-lookup"><span data-stu-id="b7937-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b7937-142"><dt>version8</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-143">Autorise l’installation d’un propriétaire de module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-143">Allow the installation of a TPM owner.</span></span> <br/> <span data-ttu-id="b7937-144">Cette opération est inversée par l’opération 9.</span><span class="sxs-lookup"><span data-stu-id="b7937-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b7937-145"><dt>0,9</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-146">Empêche l’installation d’un propriétaire de module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="b7937-147">Cette opération est inversée par l’opération 8.</span><span class="sxs-lookup"><span data-stu-id="b7937-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b7937-148"><dt>10</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-149">Activer, activer et autoriser l’installation d’un propriétaire TPM.</span><span class="sxs-lookup"><span data-stu-id="b7937-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="b7937-150">Cette opération est inversée par l’opération 11.</span><span class="sxs-lookup"><span data-stu-id="b7937-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b7937-151"><dt>11</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-152">Désactivez, désactivez et empêchez l’installation d’un propriétaire de module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="b7937-153">Cette opération est inversée par l’opération 10.</span><span class="sxs-lookup"><span data-stu-id="b7937-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="b7937-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-155">PresenceunownedFieldUpgrade physique différé</span><span class="sxs-lookup"><span data-stu-id="b7937-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="b7937-156">Le paramètre de présence physique a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="b7937-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="b7937-157"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b7937-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b7937-158"><dt>14,5</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-159">Désactivez, activez et activez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="b7937-160">Cette opération ne peut pas être inversée.</span><span class="sxs-lookup"><span data-stu-id="b7937-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b7937-161"><dt>4,5</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="b7937-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="b7937-163">Définit la configuration dont vous devez disposer physiquement pour définir le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="b7937-164">Cette opération est inversée par l’opération 16.</span><span class="sxs-lookup"><span data-stu-id="b7937-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="b7937-165"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b7937-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b7937-166"><dt>16bits</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="b7937-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="b7937-168">Définit la provision pour laquelle vous n’avez pas besoin d’être physiquement en présence pour définir le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="b7937-169">Cette opération est inversée par l’opération 15.</span><span class="sxs-lookup"><span data-stu-id="b7937-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="b7937-170"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b7937-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b7937-171"><dt>17</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="b7937-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="b7937-173">Définit la configuration dont vous devez disposer physiquement pour effacer le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="b7937-174">Cette opération est inversée par l’opération 18.</span><span class="sxs-lookup"><span data-stu-id="b7937-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="b7937-175"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b7937-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b7937-176"><dt>19</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="b7937-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="b7937-178">Définit la provision pour laquelle vous n’avez pas besoin d’être physiquement en présence pour effacer le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="b7937-179">Cette opération est inversée par l’opération 17.</span><span class="sxs-lookup"><span data-stu-id="b7937-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="b7937-180"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b7937-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b7937-181"><dt>19</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="b7937-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="b7937-183">Définit la configuration dont vous devez disposer physiquement pour gérer le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="b7937-184">Cette opération est inversée par l’opération 20.</span><span class="sxs-lookup"><span data-stu-id="b7937-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="b7937-185"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b7937-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b7937-186"><dt>20</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="b7937-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="b7937-188">Définit la configuration dont vous devez disposer physiquement pour gérer le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="b7937-189">Cette opération est inversée par l’opération 19.</span><span class="sxs-lookup"><span data-stu-id="b7937-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="b7937-190"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b7937-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b7937-191"><dt>21</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-192">Activer + activer + effacer</span><span class="sxs-lookup"><span data-stu-id="b7937-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="b7937-193">Activez, activez et désactivez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="b7937-194"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b7937-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b7937-195"><dt>22</dt> </span><span class="sxs-lookup"><span data-stu-id="b7937-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="b7937-196">Activer + activer + effacer + activer + activer</span><span class="sxs-lookup"><span data-stu-id="b7937-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="b7937-197">Activez, activez et désactivez le module de plateforme sécurisée, puis activez et réactivez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b7937-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="b7937-198"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b7937-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7937-199">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7937-199">Return value</span></span>

<span data-ttu-id="b7937-200">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7937-200">Type: **uint32**</span></span>

<span data-ttu-id="b7937-201">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="b7937-201">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="b7937-202">Le tableau suivant répertorie les codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="b7937-202">The following table lists the common return codes.</span></span>



| <span data-ttu-id="b7937-203">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b7937-203">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="b7937-204">Description</span><span class="sxs-lookup"><span data-stu-id="b7937-204">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b7937-205"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b7937-205"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="b7937-206">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="b7937-206">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="b7937-207"><dt>**Module TPM \_ \_ \_ \_ Erreur ACPI PPP**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="b7937-207"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="b7937-208">Une défaillance matérielle s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b7937-208">A hardware failure occurred.</span></span> <span data-ttu-id="b7937-209">Pour plus d'informations, consultez le fabricant de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b7937-209">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b7937-210">Notes</span><span class="sxs-lookup"><span data-stu-id="b7937-210">Remarks</span></span>

<span data-ttu-id="b7937-211">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="b7937-211">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b7937-212">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="b7937-212">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b7937-213">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="b7937-213">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b7937-214">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b7937-214">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7937-215">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7937-215">Requirements</span></span>



| <span data-ttu-id="b7937-216">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7937-216">Requirement</span></span> | <span data-ttu-id="b7937-217">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7937-217">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7937-218">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7937-218">Minimum supported client</span></span><br/> | <span data-ttu-id="b7937-219">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7937-219">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b7937-220">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7937-220">Minimum supported server</span></span><br/> | <span data-ttu-id="b7937-221">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7937-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b7937-222">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b7937-222">Namespace</span></span><br/>                | <span data-ttu-id="b7937-223">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="b7937-223">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="b7937-224">MOF</span><span class="sxs-lookup"><span data-stu-id="b7937-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7937-225"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="b7937-225"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7937-226">DLL</span><span class="sxs-lookup"><span data-stu-id="b7937-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7937-227"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="b7937-227"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7937-228">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7937-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7937-229">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="b7937-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="b7937-230">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="b7937-230">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="b7937-231">**Désactiver**</span><span class="sxs-lookup"><span data-stu-id="b7937-231">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="b7937-232">**Activer**</span><span class="sxs-lookup"><span data-stu-id="b7937-232">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="b7937-233">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="b7937-233">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="b7937-234">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="b7937-234">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
