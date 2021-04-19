---
description: Une application peut utiliser la fonction MsiOpenDatabase pour ouvrir une base de données d’installation nouvelle ou existante (fichier. msi) ou un package correctif (fichier. msp). L’application vérifie la valeur de retour de MsiOpenDatabase avant d’utiliser le handle de base de données.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Exemple de base de données et de correctif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ff5925fc409352b4c9ed8c1762ba1ad17b261f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533856"
---
# <a name="a-database-and-patch-example"></a><span data-ttu-id="2201f-103">Exemple de base de données et de correctif</span><span class="sxs-lookup"><span data-stu-id="2201f-103">A Database and Patch Example</span></span>

<span data-ttu-id="2201f-104">Une application peut utiliser la fonction [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) pour ouvrir une base de données d’installation nouvelle ou existante (fichier. msi) ou un package correctif (fichier. msp). L’application vérifie la valeur de retour de **MsiOpenDatabase** avant d’utiliser le handle de base de données.</span><span class="sxs-lookup"><span data-stu-id="2201f-104">An application can use the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function to open a new or existing installation database (.msi file) or patch package (.msp file.) The application checks the return value of **MsiOpenDatabase** before using the database handle.</span></span>

<span data-ttu-id="2201f-105">Les exemples suivants utilisent les variables de type **PMSIHANDLE** définies dans msi. h.</span><span class="sxs-lookup"><span data-stu-id="2201f-105">The following examples use the **PMSIHANDLE** type variables defined in msi.h.</span></span> <span data-ttu-id="2201f-106">Il est recommandé d’utiliser le type **PMSIHANDLE** , car le programme d’installation ferme les objets **PMSIHANDLE** à mesure qu’ils sont hors de portée, tandis que votre application doit fermer **MSIHANDLE** objets en appelant [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).</span><span class="sxs-lookup"><span data-stu-id="2201f-106">It is recommended to use the **PMSIHANDLE** type because the installer closes **PMSIHANDLE** objects as they go out of scope, whereas your application must close **MSIHANDLE** objects by calling [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).</span></span> <span data-ttu-id="2201f-107">Pour plus d’informations, consultez la section [utiliser PMSIHANDLE à la place du DEscripteur](windows-installer-best-practices.md) dans la [Windows Installer meilleures pratiques](windows-installer-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="2201f-107">For more information see [Use PMSIHANDLE instead of HANDLE](windows-installer-best-practices.md) section in the [Windows Installer Best Practices](windows-installer-best-practices.md).</span></span>

<span data-ttu-id="2201f-108">L’exemple suivant ouvre une base de données, sample.msi, en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2201f-108">The following example opens a database, sample.msi, for reading only.</span></span> <span data-ttu-id="2201f-109">[**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) fonctionne uniquement si sample.msi existe dans le répertoire c : \\ test.</span><span class="sxs-lookup"><span data-stu-id="2201f-109">[**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) succeeds only if sample.msi exists in the c:\\test directory.</span></span> <span data-ttu-id="2201f-110">En cas de réussite, le descripteur de base de données retourné peut être utilisé pour interroger les données du package d’installation à l’aide de [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) et [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).</span><span class="sxs-lookup"><span data-stu-id="2201f-110">Upon success, the returned database handle can be used to query the data in the installation package using [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) and [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).</span></span>


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



<span data-ttu-id="2201f-111">L’exemple suivant ouvre la base de données pour la lecture et l’écriture.</span><span class="sxs-lookup"><span data-stu-id="2201f-111">The following example opens the database for reading and writing.</span></span> <span data-ttu-id="2201f-112">Si l’application appelle [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), toutes les modifications apportées à la base de données sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="2201f-112">If the application calls [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), all changes made to the database are saved.</span></span> <span data-ttu-id="2201f-113">Si l’application n’appelle pas **MsiDatabaseCommit**, aucune modification n’est apportée à la base de données.</span><span class="sxs-lookup"><span data-stu-id="2201f-113">If the application does not call **MsiDatabaseCommit**, no changes are made to the database.</span></span>


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



<span data-ttu-id="2201f-114">L’exemple suivant prend une base de données existante, text.msi et crée une nouvelle base de données, newtest.msi.</span><span class="sxs-lookup"><span data-stu-id="2201f-114">The following example takes an existing database, text.msi, and creates a new database, newtest.msi.</span></span> <span data-ttu-id="2201f-115">Toutes les modifications apportées peuvent être enregistrées dans la nouvelle base de données en appelant [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="2201f-115">Any changes that are made can be saved in the new database by calling [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="2201f-116">La base de données existante spécifiée dans le paramètre *szDatabasePath* est inchangée.</span><span class="sxs-lookup"><span data-stu-id="2201f-116">The existing database specified in the *szDatabasePath* parameter is unchanged.</span></span>


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



<span data-ttu-id="2201f-117">L’exemple suivant ouvre une Windows Installer package correctif (fichier. msp) en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2201f-117">The following example opens a Windows Installer patch package (.msp file) for reading only.</span></span> <span data-ttu-id="2201f-118">Le handle de correctif renvoyé peut être utilisé pour déterminer les armoires et transformer les sous-stockages inclus dans le package de correctifs par des requêtes sur les tables [ \_ Streams](-streams-table.md) et [ \_ storages](-storages-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2201f-118">The returned patch handle can be used to determine the cabinets and transform substorages included in the patch package by queries on the [\_Streams](-streams-table.md) and [\_Storages](-storages-table.md) tables.</span></span>

<span data-ttu-id="2201f-119">**Windows Installer 2,0 :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2201f-119">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="2201f-120">À partir de Windows Installer 3,0, l’application peut interroger la [table MsiPatchSequence](msipatchsequence-table.md) présente dans un package correctif qui utilise les nouvelles informations de séquencement de correctifs.</span><span class="sxs-lookup"><span data-stu-id="2201f-120">Beginning with Windows Installer 3.0, the application can query the [MsiPatchSequence table](msipatchsequence-table.md) present in a patch package that uses the new patch sequencing information.</span></span>


```C++
PMSIHANDLE hDbPatch = 0;
LPCTSTR szPersistMode = MSIDBOPEN_READONLY + MSIDBOPEN_PATCHFILE;
UINT uiStatus4 = MsiOpenDatabase(TEXT("c:\\test\\sample.msp"), szPersistMode, &hDbPatch);
if (ERROR_SUCCESS != uiStatus4)
{
    // process error
    return uiStatus4;
}
```



 

 



