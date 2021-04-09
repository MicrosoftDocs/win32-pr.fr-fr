---
description: HKLM \\ Software \\ Microsoft \\ MSSQLSERVER \\ client.
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033657"
---
# <a name="connectto"></a><span data-ttu-id="8a3a6-103">ConnectTo</span><span class="sxs-lookup"><span data-stu-id="8a3a6-103">ConnectTo</span></span>

<span data-ttu-id="8a3a6-104">**HKLM \\ Software \\ Microsoft \\ MSSQLSERVER \\ client**</span><span class="sxs-lookup"><span data-stu-id="8a3a6-104">**HKLM\\SOFTWARE\\Microsoft\\MSSQLServer\\Client**</span></span>

## <a name="description"></a><span data-ttu-id="8a3a6-105">Description</span><span class="sxs-lookup"><span data-stu-id="8a3a6-105">Description</span></span>

<span data-ttu-id="8a3a6-106">La sous-clé **ConnectTo** stocke les informations de connexion pour les clients Windows qui se connectent aux instances du moteur de base de données Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8a3a6-106">The **ConnectTo** subkey stores connection information for Windows-based clients that connect to instances of the Microsoft SQL Server database engine.</span></span> <span data-ttu-id="8a3a6-107">Les entrées de registre de cette sous-clé sont du type de données « REG \_ SZ » et leurs valeurs spécifient les Net-Library à utiliser pour se connecter à l’instance, ainsi que tous les paramètres spécifiques au réseau.</span><span class="sxs-lookup"><span data-stu-id="8a3a6-107">Registry entries in this subkey are of data type REG\_SZ, and their values specify the Net-Library to use for connecting to the instance, as well as any network-specific parameters.</span></span>

<span data-ttu-id="8a3a6-108">Les informations de connexion stockées dans cette sous-clé sont lues par le fournisseur de OLE DB pour SQL Server, le pilote ODBC SQL Server ou la SQL Server DB-Library bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="8a3a6-108">The connection information stored in this subkey is read by the OLE DB Provider for SQL Server, the SQL Server ODBC driver, or the SQL Server DB-Library dynamic-link library (DLL).</span></span>

## <a name="change-method"></a><span data-ttu-id="8a3a6-109">Modifier la méthode</span><span class="sxs-lookup"><span data-stu-id="8a3a6-109">Change Method</span></span>

<span data-ttu-id="8a3a6-110">Vous ne devez pas modifier les entrées de cette sous-clé à l’aide de l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="8a3a6-110">You should not modify entries in this subkey by using the registry editor.</span></span> <span data-ttu-id="8a3a6-111">Utilisez l’utilitaire réseau du client SQL Server pour configurer le nom du serveur et les informations de connexion.</span><span class="sxs-lookup"><span data-stu-id="8a3a6-111">Use the SQL Server Client Network Utility to configure server name and connection information.</span></span> <span data-ttu-id="8a3a6-112">Pour obtenir des instructions supplémentaires, consultez SQL Server l’aide de l’utilitaire réseau client.</span><span class="sxs-lookup"><span data-stu-id="8a3a6-112">See SQL Server Client Network Utility Help for further instructions.</span></span>

## <a name="notes"></a><span data-ttu-id="8a3a6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8a3a6-113">Notes</span></span>

-   <span data-ttu-id="8a3a6-114">La sous-clé **ConnectTo** est utilisée par le fournisseur de OLE DB pour SQL Server, le pilote ODBC SQL Server et le SQL Server dll DB-Library.</span><span class="sxs-lookup"><span data-stu-id="8a3a6-114">The **ConnectTo** subkey is used by the OLE DB Provider for SQL Server, the SQL Server ODBC Driver, and the SQL Server DB-Library DLL.</span></span> <span data-ttu-id="8a3a6-115">Les entrées de cette sous-clé identifient les Net-Library ces composants de l’interface de programmation d’applications (API) d’accès aux données appellent.</span><span class="sxs-lookup"><span data-stu-id="8a3a6-115">Entries in this subkey identify which Net-Library these data access application programming interface (API) components call.</span></span>
-   <span data-ttu-id="8a3a6-116">Net-Libraries sont des composants SQL Server qui protègent les composants de l’API d’accès aux données des détails de l’utilisation de différentes méthodes de communication interprocessus (IPC) pour communiquer avec une instance du moteur de base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8a3a6-116">Net-Libraries are SQL Server components that shield the data access API components from the details of using different Interprocess Communication (IPC) methods to communicate with an instancess of the SQL Server database engine.</span></span>
-   <span data-ttu-id="8a3a6-117">Une mise à jour incorrecte de la sous-clé **ConnectTo** peut empêcher les applications de se connecter à une instance du moteur de base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8a3a6-117">Improperly updating the **ConnectTo** subkey might prevent applications from successfully connecting to an instance of the SQL Server database engine.</span></span>

 

 



