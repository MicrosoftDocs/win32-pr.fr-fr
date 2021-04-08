---
description: L’infrastructure de compatibilité utilise une base de données pour identifier les problèmes de compatibilité des applications et leurs solutions.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Base de données de compatibilité des applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba33ab3a8de702f2e620b7607f4d2b6904e6165
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747965"
---
# <a name="application-compatibility-database"></a><span data-ttu-id="e02f8-103">Base de données de compatibilité des applications</span><span class="sxs-lookup"><span data-stu-id="e02f8-103">Application Compatibility Database</span></span>

<span data-ttu-id="e02f8-104">L’infrastructure de compatibilité utilise une base de données pour identifier les problèmes de compatibilité des applications et leurs solutions.</span><span class="sxs-lookup"><span data-stu-id="e02f8-104">The compatibility infrastructure uses a database to identify application compatibility issues and their solutions.</span></span> <span data-ttu-id="e02f8-105">Cette base de données est un fichier binaire indexé avec une extension. sdb.</span><span class="sxs-lookup"><span data-stu-id="e02f8-105">This database is an indexed binary file with an .sdb extension.</span></span> <span data-ttu-id="e02f8-106">L’infrastructure de compatibilité fournit une interface de programmation pour accéder à la base de données.</span><span class="sxs-lookup"><span data-stu-id="e02f8-106">The compatibility infrastructure provides a programming interface to access the database.</span></span>

<span data-ttu-id="e02f8-107">Les problèmes de compatibilité peuvent être traités application par application au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e02f8-107">Compatibility issues can be addressed on an application-by-application basis at run time.</span></span> <span data-ttu-id="e02f8-108">Chaque application spécifiée dans la base de données contient un ou plusieurs composants qui ont besoin d’une solution.</span><span class="sxs-lookup"><span data-stu-id="e02f8-108">Each application specified in the database contains one or more components that need a solution.</span></span> <span data-ttu-id="e02f8-109">Les composants sont des fichiers exécutables qui sont généralement décrits à l’aide de leurs attributs de fichier (par exemple, checksum).</span><span class="sxs-lookup"><span data-stu-id="e02f8-109">Components are executable files that are generally described using their file attributes (for example, checksum).</span></span>

<span data-ttu-id="e02f8-110">Le processus de recherche de base de données et de détermination des solutions pour chaque application est appelé *correspondance*.</span><span class="sxs-lookup"><span data-stu-id="e02f8-110">The process of database lookup and determining the solutions for each application is called *matching*.</span></span> <span data-ttu-id="e02f8-111">Les attributs de fichier et la présence de fichiers associés dans le dossier ou sous-dossier contenant le fichier. exe peuvent être utilisés pour créer une correspondance unique.</span><span class="sxs-lookup"><span data-stu-id="e02f8-111">The file attributes and the presence of associated files in the folder or subfolder containing the .exe file can be used to create a unique match.</span></span> <span data-ttu-id="e02f8-112">Les fichiers associés sont appelés *fichiers correspondants*.</span><span class="sxs-lookup"><span data-stu-id="e02f8-112">The associated files are called *matching files*.</span></span>

<span data-ttu-id="e02f8-113">Une *balise* est un identificateur unique pour les entrées et les attributs de la base de données.</span><span class="sxs-lookup"><span data-stu-id="e02f8-113">A *TAG* is a unique identifier for the entries and attributes in the database.</span></span> <span data-ttu-id="e02f8-114">Le *type de balise* indique le format des données associées à la [**balise**](tag.md).</span><span class="sxs-lookup"><span data-stu-id="e02f8-114">The *TAG type* indicates the format of the data associated with the [**TAG**](tag.md).</span></span> <span data-ttu-id="e02f8-115">Par exemple, **le \_ nom de la balise** est de type **tag \_ \_ STRINGREF**; les données pour **tag \_ Name** sont une chaîne de nom.</span><span class="sxs-lookup"><span data-stu-id="e02f8-115">For example, **TAG\_NAME** is of type **TAG\_TYPE\_STRINGREF**; the data for **TAG\_NAME** is a name string.</span></span> <span data-ttu-id="e02f8-116">Un *TagId* est un pointeur vers une entrée dans une base de données particulière.</span><span class="sxs-lookup"><span data-stu-id="e02f8-116">A *TAGID* is a pointer to an entry in a particular database.</span></span> <span data-ttu-id="e02f8-117">Un *TAGREF* est un pointeur vers une entrée qui peut être utilisée sur plusieurs bases de données.</span><span class="sxs-lookup"><span data-stu-id="e02f8-117">A *TAGREF* is a pointer to an entry that can be used across multiple databases.</span></span>

<span data-ttu-id="e02f8-118">Les *attributs de fichier* sont des métadonnées associées à un fichier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="e02f8-118">*File attributes* are metadata associated with a file on disk.</span></span> <span data-ttu-id="e02f8-119">Ces attributs incluent le nom du fichier, la taille du fichier, la somme de contrôle, la version et la date.</span><span class="sxs-lookup"><span data-stu-id="e02f8-119">These attributes include the file name, file size, checksum, version, and date.</span></span> <span data-ttu-id="e02f8-120">Ces attributs sont utilisés pour déterminer si un fichier chargé par le système correspond à une entrée de base de données.</span><span class="sxs-lookup"><span data-stu-id="e02f8-120">These attributes are used to determine whether a file being loaded by the system matches a database entry.</span></span> <span data-ttu-id="e02f8-121">Par conséquent, ces attributs de fichier sont également appelés *attributs correspondants*.</span><span class="sxs-lookup"><span data-stu-id="e02f8-121">Therefore, these file attributes are also called *matching attributes*.</span></span>

## <a name="solutions"></a><span data-ttu-id="e02f8-122">Solutions</span><span class="sxs-lookup"><span data-stu-id="e02f8-122">Solutions</span></span>

<span data-ttu-id="e02f8-123">Les solutions les plus courantes appliquées aux composants d’une application sont AppHelp et AppFix.</span><span class="sxs-lookup"><span data-stu-id="e02f8-123">The most common solutions applied to the components of an application are Apphelp and Appfix.</span></span>

<span data-ttu-id="e02f8-124">Avec AppHelp, une notification de message localisée personnalisée s’affiche, généralement lorsque l’application est installée ou démarrée.</span><span class="sxs-lookup"><span data-stu-id="e02f8-124">With Apphelp, a custom localized message notification is displayed, typically when the application is installed or started.</span></span> <span data-ttu-id="e02f8-125">Il contient un bref texte qui explique le problème de compatibilité et offre la possibilité de continuer à exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="e02f8-125">It contains brief text that explains the compatibility issue and provides the option to continue running the application.</span></span> <span data-ttu-id="e02f8-126">Toutefois, certaines applications échouent considérablement et peuvent être exécutées ; AppHelp ne donne pas à l’utilisateur la possibilité de continuer à exécuter ces applications.</span><span class="sxs-lookup"><span data-stu-id="e02f8-126">However, some applications will fail dramatically is allowed to run; Apphelp will not give the user the option to continue running these applications.</span></span>

<span data-ttu-id="e02f8-127">Avec AppFix, les raccordements sont installés pour les API appelées par les composants de l’application.</span><span class="sxs-lookup"><span data-stu-id="e02f8-127">With Appfix, hooks are installed for APIs called by the components of the application.</span></span> <span data-ttu-id="e02f8-128">Ces points de raccordement pointent vers des fonctions stub qui peuvent être appelées à la place des fonctions système (également appelées « *Shiming*»).</span><span class="sxs-lookup"><span data-stu-id="e02f8-128">These hooks point to stub functions that can be called instead of the system functions (also known as *shimming*).</span></span> <span data-ttu-id="e02f8-129">Les fonctions stub effectuent les opérations nécessaires pour permettre à l’application de s’exécuter sur la version installée de Windows.</span><span class="sxs-lookup"><span data-stu-id="e02f8-129">The stub functions perform operations needed to enable the application to run on the installed version of Windows.</span></span> <span data-ttu-id="e02f8-130">Chaque fonction stub peut éventuellement appeler la fonction système après avoir terminé son travail.</span><span class="sxs-lookup"><span data-stu-id="e02f8-130">Each stub function may optionally call the system function after completing its work.</span></span> <span data-ttu-id="e02f8-131">Une *couche* ou un *mode* de compatibilité contient un ou plusieurs shims et indicateurs.</span><span class="sxs-lookup"><span data-stu-id="e02f8-131">A *compatibility layer* or *mode* contains one or more shims and flags.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e02f8-132">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e02f8-132">In this section</span></span>

-   [<span data-ttu-id="e02f8-133">**\_données APPHELP**</span><span class="sxs-lookup"><span data-stu-id="e02f8-133">**APPHELP\_DATA**</span></span>](apphelp-data.md)
-   [<span data-ttu-id="e02f8-134">**ATTRINFO**</span><span class="sxs-lookup"><span data-stu-id="e02f8-134">**ATTRINFO**</span></span>](attrinfo.md)
-   [<span data-ttu-id="e02f8-135">**BaseFlushAppcompatCache**</span><span class="sxs-lookup"><span data-stu-id="e02f8-135">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
-   [<span data-ttu-id="e02f8-136">**Rechercher des \_ informations**</span><span class="sxs-lookup"><span data-stu-id="e02f8-136">**FIND\_INFO**</span></span>](find-info.md)
-   [<span data-ttu-id="e02f8-137">**INDEXID contient**</span><span class="sxs-lookup"><span data-stu-id="e02f8-137">**INDEXID**</span></span>](indexid.md)
-   [<span data-ttu-id="e02f8-138">**TYPE de chemin \_**</span><span class="sxs-lookup"><span data-stu-id="e02f8-138">**PATH\_TYPE**</span></span>](path-type.md)
-   [<span data-ttu-id="e02f8-139">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-139">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
-   [<span data-ttu-id="e02f8-140">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="e02f8-140">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
-   [<span data-ttu-id="e02f8-141">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="e02f8-141">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
-   [<span data-ttu-id="e02f8-142">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="e02f8-142">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
-   [<span data-ttu-id="e02f8-143">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="e02f8-143">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
-   [<span data-ttu-id="e02f8-144">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="e02f8-144">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
-   [<span data-ttu-id="e02f8-145">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-145">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
-   [<span data-ttu-id="e02f8-146">**SdbFindFirstDWORDIndexedTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-146">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
-   [<span data-ttu-id="e02f8-147">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-147">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
-   [<span data-ttu-id="e02f8-148">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-148">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
-   [<span data-ttu-id="e02f8-149">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="e02f8-149">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
-   [<span data-ttu-id="e02f8-150">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="e02f8-150">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
-   [<span data-ttu-id="e02f8-151">**SdbGetAppPatchDir**</span><span class="sxs-lookup"><span data-stu-id="e02f8-151">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
-   [<span data-ttu-id="e02f8-152">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="e02f8-152">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
-   [<span data-ttu-id="e02f8-153">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="e02f8-153">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
-   [<span data-ttu-id="e02f8-154">**SdbGetFirstChild**</span><span class="sxs-lookup"><span data-stu-id="e02f8-154">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
-   [<span data-ttu-id="e02f8-155">**SdbGetIndex**</span><span class="sxs-lookup"><span data-stu-id="e02f8-155">**SdbGetIndex**</span></span>](sdbgetindex.md)
-   [<span data-ttu-id="e02f8-156">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="e02f8-156">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
-   [<span data-ttu-id="e02f8-157">**SdbGetNextChild**</span><span class="sxs-lookup"><span data-stu-id="e02f8-157">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
-   [<span data-ttu-id="e02f8-158">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="e02f8-158">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
-   [<span data-ttu-id="e02f8-159">**SdbGetTagFromTagID**</span><span class="sxs-lookup"><span data-stu-id="e02f8-159">**SdbGetTagFromTagID**</span></span>](sdbgettagfromtagid.md)
-   [<span data-ttu-id="e02f8-160">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="e02f8-160">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
-   [<span data-ttu-id="e02f8-161">**SdbIsStandardDatabase**</span><span class="sxs-lookup"><span data-stu-id="e02f8-161">**SdbIsStandardDatabase**</span></span>](sdbisstandarddatabase.md)
-   [<span data-ttu-id="e02f8-162">**SdbMakeIndexKeyFromString**</span><span class="sxs-lookup"><span data-stu-id="e02f8-162">**SdbMakeIndexKeyFromString**</span></span>](sdbmakeindexkeyfromstring.md)
-   [<span data-ttu-id="e02f8-163">**SdbOpenApphelpDetailsDatabase**</span><span class="sxs-lookup"><span data-stu-id="e02f8-163">**SdbOpenApphelpDetailsDatabase**</span></span>](sdbopenapphelpdetailsdatabase.md)
-   [<span data-ttu-id="e02f8-164">**SdbOpenApphelpResourceFile**</span><span class="sxs-lookup"><span data-stu-id="e02f8-164">**SdbOpenApphelpResourceFile**</span></span>](sdbopenapphelpresourcefile.md)
-   [<span data-ttu-id="e02f8-165">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="e02f8-165">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
-   [<span data-ttu-id="e02f8-166">**SdbQueryDataExTagID**</span><span class="sxs-lookup"><span data-stu-id="e02f8-166">**SdbQueryDataExTagID**</span></span>](sdbquerydataextagid.md)
-   [<span data-ttu-id="e02f8-167">**SDBQUERYRESULT**</span><span class="sxs-lookup"><span data-stu-id="e02f8-167">**SDBQUERYRESULT**</span></span>](sdbqueryresult.md)
-   [<span data-ttu-id="e02f8-168">**SdbReadApphelpDetailsData**</span><span class="sxs-lookup"><span data-stu-id="e02f8-168">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
-   [<span data-ttu-id="e02f8-169">**SdbReadBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-169">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
-   [<span data-ttu-id="e02f8-170">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-170">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
-   [<span data-ttu-id="e02f8-171">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-171">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
-   [<span data-ttu-id="e02f8-172">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-172">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
-   [<span data-ttu-id="e02f8-173">**SdbRegisterDatabaseEx**</span><span class="sxs-lookup"><span data-stu-id="e02f8-173">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
-   [<span data-ttu-id="e02f8-174">**SdbReleaseDatabase**</span><span class="sxs-lookup"><span data-stu-id="e02f8-174">**SdbReleaseDatabase**</span></span>](sdbreleasedatabase.md)
-   [<span data-ttu-id="e02f8-175">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="e02f8-175">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
-   [<span data-ttu-id="e02f8-176">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="e02f8-176">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
-   [<span data-ttu-id="e02f8-177">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="e02f8-177">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
-   [<span data-ttu-id="e02f8-178">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="e02f8-178">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
-   [<span data-ttu-id="e02f8-179">**SdbTagToString**</span><span class="sxs-lookup"><span data-stu-id="e02f8-179">**SdbTagToString**</span></span>](sdbtagtostring.md)
-   [<span data-ttu-id="e02f8-180">**SdbUnregisterDatabase**</span><span class="sxs-lookup"><span data-stu-id="e02f8-180">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
-   [<span data-ttu-id="e02f8-181">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-181">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
-   [<span data-ttu-id="e02f8-182">**SdbWriteBinaryTagFromFile**</span><span class="sxs-lookup"><span data-stu-id="e02f8-182">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
-   [<span data-ttu-id="e02f8-183">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-183">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
-   [<span data-ttu-id="e02f8-184">**SdbWriteNULLTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-184">**SdbWriteNULLTag**</span></span>](sdbwritenulltag.md)
-   [<span data-ttu-id="e02f8-185">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-185">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
-   [<span data-ttu-id="e02f8-186">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-186">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
-   [<span data-ttu-id="e02f8-187">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="e02f8-187">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
-   [<span data-ttu-id="e02f8-188">**Types de bases de données shim**</span><span class="sxs-lookup"><span data-stu-id="e02f8-188">**Shim Database Types**</span></span>](shim-database-types.md)
-   [<span data-ttu-id="e02f8-189">**ShimFlushCache**</span><span class="sxs-lookup"><span data-stu-id="e02f8-189">**ShimFlushCache**</span></span>](shimflushcache.md)
-   [<span data-ttu-id="e02f8-190">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e02f8-190">**TAG**</span></span>](tag.md)
-   [<span data-ttu-id="e02f8-191">**Types de BALISes**</span><span class="sxs-lookup"><span data-stu-id="e02f8-191">**TAG Types**</span></span>](tag-types.md)
-   [<span data-ttu-id="e02f8-192">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="e02f8-192">**TAGID**</span></span>](tagid.md)
-   [<span data-ttu-id="e02f8-193">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="e02f8-193">**TAGREF**</span></span>](tagref.md)

 

 



