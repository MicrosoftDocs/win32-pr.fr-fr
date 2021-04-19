---
description: Étend les propriétés définies pour les API d’ensemble de lignes.
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba37466c52f2fa9f83e3aa439ace03c1fba34f44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543734"
---
# <a name="dbpropset_msidxs_rowsetext"></a><span data-ttu-id="50a35-103">DBPROPSET \_ MSIDXS \_ ROWSETEXT</span><span class="sxs-lookup"><span data-stu-id="50a35-103">DBPROPSET\_MSIDXS\_ROWSETEXT</span></span>

<span data-ttu-id="50a35-104">Étend les propriétés définies pour les API d’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="50a35-104">Extends properties defined for the Rowset APIs.</span></span>

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

<span data-ttu-id="50a35-105">Le \_ jeu de \_ Propriétés ROWSETEXT DBPROPSET MSIDXS contient les constantes de propriété suivantes :</span><span class="sxs-lookup"><span data-stu-id="50a35-105">The DBPROPSET\_MSIDXS\_ROWSETEXT property set contains the following property constants:</span></span>

<dl> <dt>

<span data-ttu-id="50a35-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP \_ ROWSETQUERYSTATUS</span><span class="sxs-lookup"><span data-stu-id="50a35-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP\_ROWSETQUERYSTATUS</span></span>
</dt> <dd>

<span data-ttu-id="50a35-107">ID de propriété 2.</span><span class="sxs-lookup"><span data-stu-id="50a35-107">Property ID 2.</span></span> <span data-ttu-id="50a35-108">État de la requête pour l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="50a35-108">Query status for the rowset.</span></span> <span data-ttu-id="50a35-109">Les \_ \* constantes stat indiquent l’état d’exécution et de fiabilité.</span><span class="sxs-lookup"><span data-stu-id="50a35-109">The STAT\_\* constants indicate the execution and reliability status.</span></span>

</dd> <dt>

<span data-ttu-id="50a35-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>\_chaîne de \_ paramètres régionaux de commande MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="50a35-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>MSIDXSPROP\_COMMAND\_LOCALE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="50a35-111">ID de propriété 3.</span><span class="sxs-lookup"><span data-stu-id="50a35-111">Property ID 3.</span></span> <span data-ttu-id="50a35-112">Chaîne de paramètres régionaux qui représente la langue et les paramètres régionaux à utiliser pour cet ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="50a35-112">Locale string that represents the language and locale setting to use for this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="50a35-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>\_restriction de requête MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="50a35-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>MSIDXSPROP\_QUERY\_RESTRICTION</span></span>
</dt> <dd>

<span data-ttu-id="50a35-114">ID de propriété 4.</span><span class="sxs-lookup"><span data-stu-id="50a35-114">Property ID 4.</span></span> <span data-ttu-id="50a35-115">Chaîne de requête associée à cet ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="50a35-115">The query string associated with this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="50a35-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>\_arborescence d’analyse MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="50a35-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>MSIDXSPROP\_PARSE\_TREE</span></span>
</dt> <dd>

<span data-ttu-id="50a35-117">ID de propriété 5.</span><span class="sxs-lookup"><span data-stu-id="50a35-117">Property ID 5.</span></span>

</dd> <dt>

<span data-ttu-id="50a35-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>\_classement Max \_ MSIDXSPROP</span><span class="sxs-lookup"><span data-stu-id="50a35-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP\_MAX\_RANK</span></span> 
</dt> <dd>

<span data-ttu-id="50a35-119">ID de propriété 6.</span><span class="sxs-lookup"><span data-stu-id="50a35-119">Property ID 6.</span></span>

</dd> <dt>

<span data-ttu-id="50a35-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>résultats de MSIDXSPROP \_ \_ trouvés</span><span class="sxs-lookup"><span data-stu-id="50a35-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>MSIDXSPROP\_RESULTS\_FOUND</span></span>
</dt> <dd>

<span data-ttu-id="50a35-121">ID de propriété 7.</span><span class="sxs-lookup"><span data-stu-id="50a35-121">Property ID 7.</span></span>

</dd> <dt>

<span data-ttu-id="50a35-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP \_ WHEREID</span><span class="sxs-lookup"><span data-stu-id="50a35-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP\_WHEREID</span></span>
</dt> <dd>

<span data-ttu-id="50a35-123">ID de propriété 8.</span><span class="sxs-lookup"><span data-stu-id="50a35-123">Property ID 8.</span></span>

</dd> <dt>

<span data-ttu-id="50a35-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>\_version du serveur MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="50a35-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>MSIDXSPROP\_SERVER\_VERSION</span></span> 
</dt> <dd>

<span data-ttu-id="50a35-125">Nouveauté de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="50a35-125">New for Windows 7.</span></span> <span data-ttu-id="50a35-126">ID de propriété 9.</span><span class="sxs-lookup"><span data-stu-id="50a35-126">Property ID 9.</span></span> <span data-ttu-id="50a35-127">Version du serveur.</span><span class="sxs-lookup"><span data-stu-id="50a35-127">The server version.</span></span>

</dd> <dt>

<span data-ttu-id="50a35-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP \_ Server \_ winver \_ major</span><span class="sxs-lookup"><span data-stu-id="50a35-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP\_SERVER\_WINVER\_MAJOR</span></span>
</dt> <dd>

<span data-ttu-id="50a35-129">ID de propriété 10.</span><span class="sxs-lookup"><span data-stu-id="50a35-129">Property ID 10.</span></span>

</dd> <dt>

<span data-ttu-id="50a35-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>\_serveur MSIDXSPROP \_ - \_ mineur mineur</span><span class="sxs-lookup"><span data-stu-id="50a35-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP\_SERVER\_WINVER\_MINOR</span></span>
</dt> <dd>

<span data-ttu-id="50a35-131">ID de propriété 11.</span><span class="sxs-lookup"><span data-stu-id="50a35-131">Property ID 11.</span></span>

</dd> <dt>

<span data-ttu-id="50a35-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>\_serveur MSIDXSPROP \_ NLSVERSION</span><span class="sxs-lookup"><span data-stu-id="50a35-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP\_SERVER\_NLSVERSION</span></span>
</dt> <dd>

<span data-ttu-id="50a35-133">ID de propriété 12.</span><span class="sxs-lookup"><span data-stu-id="50a35-133">Property ID 12.</span></span>

</dd> <dt>

<span data-ttu-id="50a35-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP \_ Server \_ NLSVER \_ défini</span><span class="sxs-lookup"><span data-stu-id="50a35-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP\_SERVER\_NLSVER\_DEFINED</span></span> 
</dt> <dd>

<span data-ttu-id="50a35-135">ID de propriété 13.</span><span class="sxs-lookup"><span data-stu-id="50a35-135">Property ID 13.</span></span>

</dd> <dt>

<span data-ttu-id="50a35-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP \_ même \_ SORTORDER \_ utilisé</span><span class="sxs-lookup"><span data-stu-id="50a35-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP\_SAME\_SORTORDER\_USED</span></span> 
</dt> <dd>

<span data-ttu-id="50a35-137">ID de propriété 14.</span><span class="sxs-lookup"><span data-stu-id="50a35-137">Property ID 14.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50a35-138">Notes</span><span class="sxs-lookup"><span data-stu-id="50a35-138">Remarks</span></span>

<span data-ttu-id="50a35-139">Pour interroger \_ \_ la version du serveur MSIDXSPROP, il est nécessaire d’émettre la requête factice sur le serveur, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="50a35-139">To query MSIDXSPROP\_SERVER\_VERSION, it is necessary to issue the dummy query to server, such as the following example.</span></span>

`SELECT top 1 workid from servername.systemindex`

<span data-ttu-id="50a35-140">Une fois l’ensemble de lignes retourné, appelez [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour les fonctionnalités de l’ensemble de lignes, puis appelez [IRowsetInfo :: GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) pour la nouvelle propriété (MSIDXSPROP \_ Server \_ version).</span><span class="sxs-lookup"><span data-stu-id="50a35-140">After the rowset has been returned, call [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the capabilities of the rowset and then call [IRowsetInfo::GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) for the new property (MSIDXSPROP\_SERVER\_VERSION).</span></span> <span data-ttu-id="50a35-141">La propriété a un type **VT \_ I4** et peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="50a35-141">The property has a type of **VT\_I4** and can be one of the following values:</span></span>

<span data-ttu-id="50a35-142">\#définir la version de l’élément de configuration \_ \_ WDS30 0x102//258</span><span class="sxs-lookup"><span data-stu-id="50a35-142">\#define CI\_VERSION\_WDS30 0x102 // 258</span></span>

<span data-ttu-id="50a35-143">\#définir la version de l’élément de configuration \_ \_ WDS40 0x109//265</span><span class="sxs-lookup"><span data-stu-id="50a35-143">\#define CI\_VERSION\_WDS40 0x109 // 265</span></span>

<span data-ttu-id="50a35-144">\#définir la version de l’élément de configuration \_ \_ WIN70 0X700//1792</span><span class="sxs-lookup"><span data-stu-id="50a35-144">\#define CI\_VERSION\_WIN70 0x700 // 1792</span></span>

<span data-ttu-id="50a35-145">Une fois que la valeur est connue, le client peut former une requête prise en charge par le serveur et émettre une requête réelle.</span><span class="sxs-lookup"><span data-stu-id="50a35-145">Once the value is known, the client can form a query which is supported by the server and issue a real query.</span></span>

<span data-ttu-id="50a35-146">DBPROPSET \_ MSIDXS \_ ROWSETEXT est déclaré dans NTQuery. h.</span><span class="sxs-lookup"><span data-stu-id="50a35-146">DBPROPSET\_MSIDXS\_ROWSETEXT is declared in ntquery.h.</span></span>

 

 
