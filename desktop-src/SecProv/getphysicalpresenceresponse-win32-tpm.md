---
description: Retourne les résultats d’une opération de présence physique TPM effectuée.
ms.assetid: 28d76149-3905-45db-a41e-32fac1603582
title: Méthode GetPhysicalPresenceResponse de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceResponse
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 47dfad1491b398b035e40867d10d2d3e46327dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515990"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a><span data-ttu-id="569a3-103">Méthode GetPhysicalPresenceResponse de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="569a3-103">GetPhysicalPresenceResponse method of the Win32\_Tpm class</span></span>

<span data-ttu-id="569a3-104">La méthode **GetPhysicalPresenceResponse** de la [**classe \_ TPM Win32**](win32-tpm.md) retourne les résultats d’une opération de présence physique TPM qui a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="569a3-104">The **GetPhysicalPresenceResponse** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the results from a TPM physical presence operation that was performed.</span></span> <span data-ttu-id="569a3-105">Utilisez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) pour demander une opération.</span><span class="sxs-lookup"><span data-stu-id="569a3-105">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="569a3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="569a3-106">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceResponse(
  [out] uint32 Request,
  [out] uint32 Response
);
```



## <a name="parameters"></a><span data-ttu-id="569a3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="569a3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="569a3-108">*Demande* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="569a3-108">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="569a3-109">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="569a3-109">Type: **uint32**</span></span>

<span data-ttu-id="569a3-110">Valeur entière qui spécifie l’opération de présence physique TPM effectuée.</span><span class="sxs-lookup"><span data-stu-id="569a3-110">An integer value that specifies the TPM physical presence operation that was performed.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="569a3-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="569a3-111">Value</span></span></th>
<th><span data-ttu-id="569a3-112">Signification</span><span class="sxs-lookup"><span data-stu-id="569a3-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="569a3-113"><dt>entre</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-113"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-114">Aucune demande.</span><span class="sxs-lookup"><span data-stu-id="569a3-114">No request.</span></span><br/> <span data-ttu-id="569a3-115">Aucune opération de présence physique n’a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="569a3-115">No physical presence operation was performed.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="569a3-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-117">Activez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-117">Enable the TPM.</span></span><br/> <span data-ttu-id="569a3-118">Cette opération est inversée par l’opération 2.</span><span class="sxs-lookup"><span data-stu-id="569a3-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="569a3-119">Pour plus d’informations, consultez les méthodes associées qui n’impliquent pas de présence physique :</span><span class="sxs-lookup"><span data-stu-id="569a3-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="569a3-120"><a href="enable-win32-tpm.md"><strong>Activer</strong></a></span><span class="sxs-lookup"><span data-stu-id="569a3-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="569a3-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="569a3-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="569a3-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-123">Désactivez le module TPM.</span><span class="sxs-lookup"><span data-stu-id="569a3-123">Disable the TPM.</span></span><br/> <span data-ttu-id="569a3-124">Cette opération est inversée par l’opération 1.</span><span class="sxs-lookup"><span data-stu-id="569a3-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="569a3-125">Pour plus d’informations, consultez cette méthode associée qui n’implique pas de présence physique : <a href="disable-win32-tpm.md"><strong>Désactiver</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="569a3-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="569a3-126"><dt>1,3</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-127">Activez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-127">Activate the TPM.</span></span><br/> <span data-ttu-id="569a3-128">Cette opération est inversée par l’opération 4.</span><span class="sxs-lookup"><span data-stu-id="569a3-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="569a3-129"><dt>4</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-130">Désactivez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="569a3-131">Cette opération est inversée par l’opération 3.</span><span class="sxs-lookup"><span data-stu-id="569a3-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="569a3-132"><dt>5,5</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-133">Effacez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-133">Clear the TPM.</span></span><br/> <span data-ttu-id="569a3-134">Cette opération ne peut pas être inversée.</span><span class="sxs-lookup"><span data-stu-id="569a3-134">This operation cannot be reversed.</span></span> <br/> <span data-ttu-id="569a3-135">Pour plus d’informations, consultez cette méthode associée qui n’implique pas la présence physique : <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="569a3-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="569a3-136"><dt>6,3</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-137">Activez et activez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-137">Enable and activate the TPM.</span></span><br/> <span data-ttu-id="569a3-138">Cette opération est inversée par l’opération 7.</span><span class="sxs-lookup"><span data-stu-id="569a3-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="569a3-139"><dt>Commission(7</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-140">Désactivez et désactivez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="569a3-141">Cette opération est inversée par l’opération 6.</span><span class="sxs-lookup"><span data-stu-id="569a3-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="569a3-142"><dt>version8</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-143">Autorise l’installation d’un propriétaire de module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-143">Allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="569a3-144">Cette opération est inversée par l’opération 9.</span><span class="sxs-lookup"><span data-stu-id="569a3-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="569a3-145"><dt>0,9</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-146">Empêche l’installation d’un propriétaire de module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="569a3-147">Cette opération est inversée par l’opération 8.</span><span class="sxs-lookup"><span data-stu-id="569a3-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="569a3-148"><dt>10</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-149">Activer, activer et autoriser l’installation d’un propriétaire TPM.</span><span class="sxs-lookup"><span data-stu-id="569a3-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="569a3-150">Cette opération est inversée par l’opération 11.</span><span class="sxs-lookup"><span data-stu-id="569a3-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="569a3-151"><dt>11</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-152">Désactivez, désactivez et empêchez l’installation d’un propriétaire de module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="569a3-153">Cette opération est inversée par l’opération 10.</span><span class="sxs-lookup"><span data-stu-id="569a3-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="569a3-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-155">PresenceunownedFieldUpgrade physique différé</span><span class="sxs-lookup"><span data-stu-id="569a3-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="569a3-156">Le paramètre de présence physique a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="569a3-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="569a3-157"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="569a3-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="569a3-158"><dt>14,5</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-159">Désactivez, activez et activez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="569a3-160">Cette opération ne peut pas être inversée.</span><span class="sxs-lookup"><span data-stu-id="569a3-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="569a3-161"><dt>4,5</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="569a3-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="569a3-163">Définit la configuration dont vous devez disposer physiquement pour définir le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="569a3-164">Cette opération est inversée par l’opération 16.</span><span class="sxs-lookup"><span data-stu-id="569a3-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="569a3-165"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="569a3-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="569a3-166"><dt>16bits</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="569a3-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="569a3-168">Définit la provision pour laquelle vous n’avez pas besoin d’être physiquement en présence pour définir le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="569a3-169">Cette opération est inversée par l’opération 15.</span><span class="sxs-lookup"><span data-stu-id="569a3-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="569a3-170"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="569a3-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="569a3-171"><dt>17</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="569a3-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="569a3-173">Définit la configuration dont vous devez disposer physiquement pour effacer le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="569a3-174">Cette opération est inversée par l’opération 18.</span><span class="sxs-lookup"><span data-stu-id="569a3-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="569a3-175"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="569a3-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="569a3-176"><dt>19</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="569a3-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="569a3-178">Définit la provision pour laquelle vous n’avez pas besoin d’être physiquement en présence pour effacer le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="569a3-179">Cette opération est inversée par l’opération 17.</span><span class="sxs-lookup"><span data-stu-id="569a3-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="569a3-180"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="569a3-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="569a3-181"><dt>19</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="569a3-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="569a3-183">Définit la configuration dont vous devez disposer physiquement pour gérer le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="569a3-184">Cette opération est inversée par l’opération 20.</span><span class="sxs-lookup"><span data-stu-id="569a3-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="569a3-185"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="569a3-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="569a3-186"><dt>20</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="569a3-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="569a3-188">Définit la configuration dont vous devez disposer physiquement pour gérer le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="569a3-189">Cette opération est inversée par l’opération 19.</span><span class="sxs-lookup"><span data-stu-id="569a3-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="569a3-190"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="569a3-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="569a3-191"><dt>21</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-192">Activer + activer + effacer</span><span class="sxs-lookup"><span data-stu-id="569a3-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="569a3-193">Activez, activez et désactivez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="569a3-194"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="569a3-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="569a3-195"><dt>22</dt> </span><span class="sxs-lookup"><span data-stu-id="569a3-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="569a3-196">Activer + activer + effacer + activer + activer</span><span class="sxs-lookup"><span data-stu-id="569a3-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="569a3-197">Activez, activez et désactivez le module de plateforme sécurisée, puis activez et réactivez le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="569a3-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="569a3-198"><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="569a3-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="569a3-199">*Réponse* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="569a3-199">*Response* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="569a3-200">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="569a3-200">Type: **uint32**</span></span>

<span data-ttu-id="569a3-201">Valeur entière qui spécifie les résultats de l’exécution de l’opération de présence physique TPM.</span><span class="sxs-lookup"><span data-stu-id="569a3-201">An integer value that specifies the results of performing the TPM physical presence operation.</span></span>

<span data-ttu-id="569a3-202">Une opération de présence physique est réussie si un utilisateur physiquement présent confirme l’opération et si l’opération s’exécute sans erreur.</span><span class="sxs-lookup"><span data-stu-id="569a3-202">A physical presence operation is successful if a physically present user confirms the operation and if the operation runs without errors.</span></span>

<span data-ttu-id="569a3-203">Cette valeur peut contenir toute erreur TPM.</span><span class="sxs-lookup"><span data-stu-id="569a3-203">This value may contain any TPM error.</span></span> <span data-ttu-id="569a3-204">Le tableau suivant répertorie quelques-unes des réponses d’erreur courantes.</span><span class="sxs-lookup"><span data-stu-id="569a3-204">The following table lists some of the common error responses.</span></span>



| <span data-ttu-id="569a3-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="569a3-205">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="569a3-206">Signification</span><span class="sxs-lookup"><span data-stu-id="569a3-206">Meaning</span></span>                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="569a3-207"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-207"><dt>0</dt></span></span> </dl>                                                                                                                                                                                             | <span data-ttu-id="569a3-208">L’opération TPM demandée a réussi.</span><span class="sxs-lookup"><span data-stu-id="569a3-208">The requested TPM operation was successful.</span></span><br/>              |
| <span id="TPM_E_PPI_USER_ABORT"></span><span id="tpm_e_ppi_user_abort"></span><dl> <span data-ttu-id="569a3-209"><dt>**Module TPM \_ E \_ PPP \_ utilisateur \_ Abort**</dt> <dt>2150171393 (0x80290301)</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-209"><dt>**TPM\_E\_PPI\_USER\_ABORT**</dt> <dt>2150171393 (0x80290301)</dt></span></span> </dl>       | <span data-ttu-id="569a3-210">L’utilisateur a refusé l’opération TPM demandée.</span><span class="sxs-lookup"><span data-stu-id="569a3-210">The user rejected the requested TPM operation.</span></span><br/>           |
| <span id="TPM_E_PPI_BIOS_FAILURE"></span><span id="tpm_e_ppi_bios_failure"></span><dl> <span data-ttu-id="569a3-211"><dt>**Module TPM \_ \_ \_ \_ Erreur du BIOS E-PPP**</dt> <dt>2150171394 (0x80290302)</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-211"><dt>**TPM\_E\_PPI\_BIOS\_FAILURE**</dt> <dt>2150171394 (0x80290302)</dt></span></span> </dl> | <span data-ttu-id="569a3-212">Une défaillance du BIOS s’est produite lors de l’exécution de l’opération TPM.</span><span class="sxs-lookup"><span data-stu-id="569a3-212">A BIOS failure occurred while running the TPM operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="569a3-213">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="569a3-213">Return value</span></span>

<span data-ttu-id="569a3-214">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="569a3-214">Type: **uint32**</span></span>

<span data-ttu-id="569a3-215">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="569a3-215">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="569a3-216">Le tableau suivant répertorie certains des codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="569a3-216">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="569a3-217">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="569a3-217">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="569a3-218">Description</span><span class="sxs-lookup"><span data-stu-id="569a3-218">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="569a3-219"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-219"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="569a3-220">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="569a3-220">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="569a3-221"><dt>**Module TPM \_ \_ \_ \_ Erreur ACPI PPP**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-221"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="569a3-222">Une défaillance matérielle s’est produite.</span><span class="sxs-lookup"><span data-stu-id="569a3-222">A hardware failure occurred.</span></span> <span data-ttu-id="569a3-223">Pour plus d'informations, consultez le fabricant de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="569a3-223">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="569a3-224">Notes</span><span class="sxs-lookup"><span data-stu-id="569a3-224">Remarks</span></span>

<span data-ttu-id="569a3-225">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="569a3-225">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="569a3-226">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="569a3-226">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="569a3-227">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="569a3-227">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="569a3-228">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="569a3-228">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="569a3-229">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="569a3-229">Requirements</span></span>



| <span data-ttu-id="569a3-230">Condition requise</span><span class="sxs-lookup"><span data-stu-id="569a3-230">Requirement</span></span> | <span data-ttu-id="569a3-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="569a3-231">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="569a3-232">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="569a3-232">Minimum supported client</span></span><br/> | <span data-ttu-id="569a3-233">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="569a3-233">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="569a3-234">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="569a3-234">Minimum supported server</span></span><br/> | <span data-ttu-id="569a3-235">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="569a3-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="569a3-236">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="569a3-236">Namespace</span></span><br/>                | <span data-ttu-id="569a3-237">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="569a3-237">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="569a3-238">MOF</span><span class="sxs-lookup"><span data-stu-id="569a3-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="569a3-239"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-239"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="569a3-240">DLL</span><span class="sxs-lookup"><span data-stu-id="569a3-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="569a3-241"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="569a3-241"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="569a3-242">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="569a3-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="569a3-243">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="569a3-243">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="569a3-244">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="569a3-244">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="569a3-245">**Désactiver**</span><span class="sxs-lookup"><span data-stu-id="569a3-245">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="569a3-246">**Activer**</span><span class="sxs-lookup"><span data-stu-id="569a3-246">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="569a3-247">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="569a3-247">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> </dl>

 

 
