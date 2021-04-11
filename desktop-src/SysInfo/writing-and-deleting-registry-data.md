---
description: Une application peut utiliser la fonction RegSetValueEx pour associer une valeur et ses données à une clé. Pour obtenir la liste des types de valeurs pris en charge par RegSetValueEx, consultez types de valeur de registre.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Écriture et suppression de données de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5185c98f39a37512ec56fb994d5f1c4ba4b61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318989"
---
# <a name="writing-and-deleting-registry-data"></a><span data-ttu-id="55b9c-104">Écriture et suppression de données de Registre</span><span class="sxs-lookup"><span data-stu-id="55b9c-104">Writing and Deleting Registry Data</span></span>

<span data-ttu-id="55b9c-105">Une application peut utiliser la fonction [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) pour associer une valeur et ses données à une clé.</span><span class="sxs-lookup"><span data-stu-id="55b9c-105">An application can use the [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) function to associate a value and its data with a key.</span></span> <span data-ttu-id="55b9c-106">Pour obtenir la liste des types de valeurs pris en charge par **RegSetValueEx**, consultez [types de valeur de registre](registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="55b9c-106">For a list of the value types supported by **RegSetValueEx**, see [Registry Value Types](registry-value-types.md).</span></span>

<span data-ttu-id="55b9c-107">Pour supprimer une valeur d’une clé, une application peut utiliser la fonction [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) .</span><span class="sxs-lookup"><span data-stu-id="55b9c-107">To delete a value from a key, an application can use the [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) function.</span></span> <span data-ttu-id="55b9c-108">Pour supprimer une clé, elle peut utiliser la fonction [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) .</span><span class="sxs-lookup"><span data-stu-id="55b9c-108">To delete a key, it can use the [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) function.</span></span> <span data-ttu-id="55b9c-109">Une clé supprimée n’est pas supprimée tant que le dernier descripteur n’a pas été fermé.</span><span class="sxs-lookup"><span data-stu-id="55b9c-109">A deleted key is not removed until the last handle to it has been closed.</span></span> <span data-ttu-id="55b9c-110">Les sous-clés et les valeurs ne peuvent pas être créées sous une clé supprimée.</span><span class="sxs-lookup"><span data-stu-id="55b9c-110">Subkeys and values cannot be created under a deleted key.</span></span>

<span data-ttu-id="55b9c-111">Il n’est pas possible de verrouiller une clé de Registre pendant une opération d’écriture pour synchroniser l’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="55b9c-111">It is not possible to lock a registry key during a write operation to synchronize access to the data.</span></span> <span data-ttu-id="55b9c-112">Toutefois, vous pouvez contrôler l’accès à une clé de Registre à l’aide des attributs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="55b9c-112">However, you can control access to a registry key using security attributes.</span></span> <span data-ttu-id="55b9c-113">Pour plus d’informations, consultez sécurité de la [clé de Registre et droits d’accès](registry-key-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="55b9c-113">For more information, see [Registry Key Security and Access Rights](registry-key-security-and-access-rights.md).</span></span>

<span data-ttu-id="55b9c-114">Plusieurs opérations de Registre peuvent être effectuées au sein d’une même transaction.</span><span class="sxs-lookup"><span data-stu-id="55b9c-114">More than one registry operation can be performed within a single transaction.</span></span> <span data-ttu-id="55b9c-115">Pour associer une clé de Registre à une transaction, une application peut utiliser la fonction [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) ou [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="55b9c-115">To associate a registry key with a transaction, an application can use the [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) or [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) function.</span></span> <span data-ttu-id="55b9c-116">Pour plus d’informations sur les transactions, consultez [Gestionnaire de transactions du noyau](/windows/desktop/Ktm/kernel-transaction-manager-portal).</span><span class="sxs-lookup"><span data-stu-id="55b9c-116">For more information about transactions, see [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).</span></span>

 

 
