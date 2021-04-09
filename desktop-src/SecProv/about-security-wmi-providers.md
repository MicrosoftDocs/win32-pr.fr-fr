---
description: Autorisez les applications à interagir avec le Module de plateforme sécurisée (TPM) (TPM) et Chiffrement de lecteur BitLocker (BDE) par le biais de l’infrastructure de gestion unifiée de Windows Management Instrumentation (WMI).
ms.assetid: acd1bc8e-3311-47f9-88b1-739f224e40e9
title: À propos des fournisseurs WMI de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed75cebf14ee3eb419578111b7de15608661d91e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952619"
---
# <a name="about-security-wmi-providers"></a><span data-ttu-id="57536-103">À propos des fournisseurs WMI de sécurité</span><span class="sxs-lookup"><span data-stu-id="57536-103">About Security WMI Providers</span></span>

<span data-ttu-id="57536-104">Les fournisseurs WMI de sécurité permettent aux applications d’interagir avec le Module de plateforme sécurisée (TPM) (TPM) et Chiffrement de lecteur BitLocker (BDE) par le biais de l’infrastructure de gestion unifiée de Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="57536-104">The Security WMI Providers allow applications to interact with the Trusted Platform Module (TPM) and BitLocker Drive Encryption (BDE) through the unified management framework of Windows Management Instrumentation (WMI).</span></span>



| <span data-ttu-id="57536-105">Section</span><span class="sxs-lookup"><span data-stu-id="57536-105">Section</span></span>                                                                  | <span data-ttu-id="57536-106">Description</span><span class="sxs-lookup"><span data-stu-id="57536-106">Description</span></span>                                                                                                                    |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57536-107">Informations de référence sur les fournisseurs WMI de sécurité</span><span class="sxs-lookup"><span data-stu-id="57536-107">Security WMI Providers Reference</span></span>](security-wmi-providers-reference.md) | <span data-ttu-id="57536-108">Documentation API pour [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) et les classes [**\_ TPM Win32**](win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="57536-108">API documentation for [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) and [**Win32\_Tpm**](win32-tpm.md) classes.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="57536-109">Notes</span><span class="sxs-lookup"><span data-stu-id="57536-109">Remarks</span></span>

<span data-ttu-id="57536-110">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="57536-110">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="57536-111">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="57536-111">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="57536-112">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="57536-112">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="57536-113">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="57536-113">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

 

 
