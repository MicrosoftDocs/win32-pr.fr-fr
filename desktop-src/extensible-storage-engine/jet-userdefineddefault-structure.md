---
description: 'En savoir plus sur : structure JET_USERDEFINEDDEFAULT'
title: Structure JET_USERDEFINEDDEFAULT
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520756"
---
# <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="2856e-103">Structure JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="2856e-103">JET_USERDEFINEDDEFAULT Structure</span></span>


<span data-ttu-id="2856e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="2856e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="2856e-105">Structure JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="2856e-105">JET_USERDEFINEDDEFAULT Structure</span></span>

<span data-ttu-id="2856e-106">La structure **JET_USERDEFINEDDEFAULT** est spécifiée conjointement avec JET_bitColumnUserDefinedDefault pour attribuer une valeur par défaut à une nouvelle colonne qui est déterminée à l’aide d’un rappel.</span><span class="sxs-lookup"><span data-stu-id="2856e-106">The **JET_USERDEFINEDDEFAULT** structure is specified in conjunction with JET_bitColumnUserDefinedDefault to give a new column a default value that is determined using a callback.</span></span> <span data-ttu-id="2856e-107">Cette technique peut être utilisée pour implémenter des colonnes calculées.</span><span class="sxs-lookup"><span data-stu-id="2856e-107">This technique can be used to implement computed columns.</span></span>

<span data-ttu-id="2856e-108">**Windows XP :** La structure **JET_USERDEFINEDDEFAULT** est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2856e-108">**Windows XP:** The **JET_USERDEFINEDDEFAULT** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a><span data-ttu-id="2856e-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2856e-109">Members</span></span>

<span data-ttu-id="2856e-110">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="2856e-110">**szCallback**</span></span>

<span data-ttu-id="2856e-111">Nom d’exportation de la fonction qui implémente le rappel au format « \! fonction de module ».</span><span class="sxs-lookup"><span data-stu-id="2856e-111">The export name of the function that implements the callback in "module\!function" format.</span></span>

<span data-ttu-id="2856e-112">Le rappel est conservé dans le cadre du schéma de colonne.</span><span class="sxs-lookup"><span data-stu-id="2856e-112">The callback persists as a part of the column schema.</span></span> <span data-ttu-id="2856e-113">L’exécutable hôte et le nom d’exportation réels de la fonction doivent être rendus persistants pour permettre la recherche de l’adresse réelle de la fonction au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="2856e-113">The actual host executable and export name of the function must persist to enable the lookup of the true address of the function at run time.</span></span>

<span data-ttu-id="2856e-114">Le nom du module est le nom du fichier binaire hôte qui contient la fonction.</span><span class="sxs-lookup"><span data-stu-id="2856e-114">The module name is the name of the host binary that contains the function.</span></span> <span data-ttu-id="2856e-115">Le nom de la fonction est le nom de l’exportation pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="2856e-115">The function name is the name of the export for that function.</span></span> <span data-ttu-id="2856e-116">Ces deux informations seront utilisées par le moteur de base de données au moment de l’exécution pour localiser l’adresse réelle du rappel en exécutant un appel [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) sur le nom du module, suivi d’un appel [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) sur le nom de la fonction.</span><span class="sxs-lookup"><span data-stu-id="2856e-116">These two pieces of information will be used by the database engine at runtime to locate the true address of the callback by executing a [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) call on the module name followed by a [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) call on the function name.</span></span>

<span data-ttu-id="2856e-117">Par exemple, si le rappel a été implémenté dans une DLL nommée MyCallback.DLL et que cette DLL était stockée dans C : \\ MyApplication et que la fonction implémentant le rappel a été exportée à partir de la dll en tant que UserDefinedDefaultCallback, la chaîne requise serait « C : \\ MyApplication \\MyCallback.DLL\! UserDefinedDefaultCallback ».</span><span class="sxs-lookup"><span data-stu-id="2856e-117">For example, if the callback were implemented in a DLL called MyCallback.DLL and that DLL were stored in C:\\MyApplication and the function implementing the callback were exported from the DLL as UserDefinedDefaultCallback, then the required string would be "C:\\MyApplication\\MyCallback.DLL\!UserDefinedDefaultCallback".</span></span>

<span data-ttu-id="2856e-118">**Remarque**  «» Incorporé \!</span><span class="sxs-lookup"><span data-stu-id="2856e-118">**Note**  Embedded "\!"</span></span> <span data-ttu-id="2856e-119">les caractères de la partie module du nom de rappel ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2856e-119">characters in the module portion of the callback name are not supported.</span></span>

<span data-ttu-id="2856e-120">Il est fortement recommandé d’utiliser un nom de rappel qui n’est pas une fonction de l’architecture de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="2856e-120">It is highly recommended that you use a callback name that is not a function of the host architecture.</span></span> <span data-ttu-id="2856e-121">Par exemple, n’utilisez pas d’exportations décorées comme stdcall ( UserDefinedDefaultCallback@32 ), car cette Convention d’appel est uniquement prise en charge sur les ordinateurs x86.</span><span class="sxs-lookup"><span data-stu-id="2856e-121">For example, do not use exports decorated as stdcall (UserDefinedDefaultCallback@32) because this calling convention is only supported on x86 machines.</span></span> <span data-ttu-id="2856e-122">Si un rappel de ce type a été utilisé, la base de données ne peut être utilisée que sur un ordinateur x86.</span><span class="sxs-lookup"><span data-stu-id="2856e-122">If such a callback were used then the database could only be used on an x86 machine.</span></span> <span data-ttu-id="2856e-123">Dans ce cas, vous devez utiliser un alias pour effectuer une exportation non indépendante de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="2856e-123">An alias should be used to make a platform-agnostic export in this case.</span></span>

<span data-ttu-id="2856e-124">Il est fortement recommandé d’utiliser le chemin d’accès complet du nom du module qui implémente le rappel.</span><span class="sxs-lookup"><span data-stu-id="2856e-124">It is highly recommended that you use the full path of the module name that is implementing the callback.</span></span> <span data-ttu-id="2856e-125">Si un chemin d’accès relatif est utilisé, le processus qui héberge la base de données peut être vulnérable aux attaques par un binaire non autorisé.</span><span class="sxs-lookup"><span data-stu-id="2856e-125">If a relative path is used then the process that is hosting the database might be susceptible to attack by a rogue binary.</span></span>

<span data-ttu-id="2856e-126">L’application doit passer uniquement les rappels approuvés au moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="2856e-126">The application should pass only trusted callbacks to the database engine.</span></span> <span data-ttu-id="2856e-127">Le moteur de base de données chargera le fichier binaire pour vérifier son existence lors de la création de la colonne associée.</span><span class="sxs-lookup"><span data-stu-id="2856e-127">The database engine will load the binary to verify its existence when the associated column is created.</span></span> <span data-ttu-id="2856e-128">Si le chemin d’accès au fichier binaire n’est pas validé ou connu comme approuvé, il peut attaquer le processus qui héberge la base de données.</span><span class="sxs-lookup"><span data-stu-id="2856e-128">If the path to the binary is not validated or known to be trusted then it could attack the process that is hosting the database.</span></span>

<span data-ttu-id="2856e-129">**pbUserData**</span><span class="sxs-lookup"><span data-stu-id="2856e-129">**pbUserData**</span></span>

<span data-ttu-id="2856e-130">Bloc autonome de données définies par l’utilisateur à passer au rappel lorsqu’il est appelé. Le bloc de données fourni est conservé en tant que partie du schéma de colonne.</span><span class="sxs-lookup"><span data-stu-id="2856e-130">A self-contained block of user-defined data to be passed to the callback when invoked.The data block that is provided will persist as a part of the column schema.</span></span> <span data-ttu-id="2856e-131">Par conséquent, le bloc de données doit être entièrement autonome et ne peut pas faire référence à des données qui se trouvent en dehors de la portée de la base de données.</span><span class="sxs-lookup"><span data-stu-id="2856e-131">As a result, the data block must be entirely self-contained and cannot refer to any data that is outside the scope of the database.</span></span>

<span data-ttu-id="2856e-132">Si **pbUserData** est égal à zéro, la valeur de **cbUserData** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="2856e-132">If **pbUserData** is zero then the value of **cbUserData** is ignored.</span></span> <span data-ttu-id="2856e-133">Dans ce cas, aucune donnée définie par l’utilisateur n’est passée au rappel lorsqu’il est appelé.</span><span class="sxs-lookup"><span data-stu-id="2856e-133">In this case, no user-defined data will be passed to the callback when invoked.</span></span>

<span data-ttu-id="2856e-134">**cbUserData**</span><span class="sxs-lookup"><span data-stu-id="2856e-134">**cbUserData**</span></span>

<span data-ttu-id="2856e-135">Consultez **pbUserData**.</span><span class="sxs-lookup"><span data-stu-id="2856e-135">See **pbUserData**.</span></span>

<span data-ttu-id="2856e-136">**szDependantColumns**</span><span class="sxs-lookup"><span data-stu-id="2856e-136">**szDependantColumns**</span></span>

<span data-ttu-id="2856e-137">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="2856e-137">Reserved for future use.</span></span>

<span data-ttu-id="2856e-138">Ce membre doit toujours avoir la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="2856e-138">This member should always be set to NULL.</span></span>

### <a name="requirements"></a><span data-ttu-id="2856e-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2856e-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2856e-140"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2856e-140"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2856e-141">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="2856e-141">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2856e-142"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="2856e-142"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2856e-143">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2856e-143">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2856e-144"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="2856e-144"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2856e-145">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="2856e-145">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2856e-146"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2856e-146"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2856e-147">Implémenté comme <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) et <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2856e-147">Implemented as <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) and <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2856e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2856e-148">See Also</span></span>

[<span data-ttu-id="2856e-149">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="2856e-149">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="2856e-150">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="2856e-150">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="2856e-151">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="2856e-151">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)
