---
description: 'En savoir plus sur les éléments suivants : ColumnStream'
title: Membres ColumnStream
TOCTitle: ColumnStream members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream_members(v=EXCHG.10)
ms:contentKeyID: 55101147
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9f35c0e000329bc98e2f9fd5873cd724516271d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564717"
---
# <a name="columnstream-members"></a><span data-ttu-id="e618d-103">Membres ColumnStream</span><span class="sxs-lookup"><span data-stu-id="e618d-103">ColumnStream members</span></span>

<span data-ttu-id="e618d-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="e618d-104">Include protected members</span></span>  
<span data-ttu-id="e618d-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="e618d-105">Include inherited members</span></span>  

<span data-ttu-id="e618d-106">Cette classe fournit une interface de streaming à une colonne de valeur longue (par exemple, une colonne de type [LONGBINARY](./jet-coltyp-enumeration.md) ou [LONGTEXT](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="e618d-106">This class provides a streaming interface to a long-value column (i.e. a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="e618d-107">Le type [ColumnStream](./columnstream-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="e618d-107">The [ColumnStream](./columnstream-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="e618d-108">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="e618d-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e618d-109">Nom</span><span class="sxs-lookup"><span data-stu-id="e618d-109">Name</span></span></th>
<th><span data-ttu-id="e618d-110">Description</span><span class="sxs-lookup"><span data-stu-id="e618d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-112"><a href="dn334142(v=exchg.10).md">ColumnStream</a></span><span class="sxs-lookup"><span data-stu-id="e618d-112"><a href="dn334142(v=exchg.10).md">ColumnStream</a></span></span></td>
<td><span data-ttu-id="e618d-113">Initialise une nouvelle instance de la classe ColumnStream.</span><span class="sxs-lookup"><span data-stu-id="e618d-113">Initializes a new instance of the ColumnStream class.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e618d-114">Haut</span><span class="sxs-lookup"><span data-stu-id="e618d-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="e618d-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e618d-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e618d-116">Nom</span><span class="sxs-lookup"><span data-stu-id="e618d-116">Name</span></span></th>
<th><span data-ttu-id="e618d-117">Description</span><span class="sxs-lookup"><span data-stu-id="e618d-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e618d-119"><a href="dn334201(v=exchg.10).md">CanRead</a></span><span class="sxs-lookup"><span data-stu-id="e618d-119"><a href="dn334201(v=exchg.10).md">CanRead</a></span></span></td>
<td><span data-ttu-id="e618d-120">Obtient une valeur indiquant si le flux prend en charge la lecture.</span><span class="sxs-lookup"><span data-stu-id="e618d-120">Gets a value indicating whether the stream supports reading.</span></span> <span data-ttu-id="e618d-121">(Substitue <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream. CanRead</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-121">(Overrides <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream.CanRead</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e618d-123"><a href="dn334153(v=exchg.10).md">CanSeek</a></span><span class="sxs-lookup"><span data-stu-id="e618d-123"><a href="dn334153(v=exchg.10).md">CanSeek</a></span></span></td>
<td><span data-ttu-id="e618d-124">Obtient une valeur indiquant si le flux prend en charge la recherche.</span><span class="sxs-lookup"><span data-stu-id="e618d-124">Gets a value indicating whether the stream supports seeking.</span></span> <span data-ttu-id="e618d-125">(Substitue <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream. CanSeek</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-125">(Overrides <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream.CanSeek</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e618d-127"><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></span><span class="sxs-lookup"><span data-stu-id="e618d-127"><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></span></span></td>
<td><span data-ttu-id="e618d-128">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-128">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e618d-130"><a href="dn334204(v=exchg.10).md">CanWrite</a></span><span class="sxs-lookup"><span data-stu-id="e618d-130"><a href="dn334204(v=exchg.10).md">CanWrite</a></span></span></td>
<td><span data-ttu-id="e618d-131">Obtient une valeur indiquant si le flux prend en charge l'écriture.</span><span class="sxs-lookup"><span data-stu-id="e618d-131">Gets a value indicating whether the stream supports writing.</span></span> <span data-ttu-id="e618d-132">(Substitue <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream. CanWrite</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-132">(Overrides <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream.CanWrite</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e618d-134"><a href="dn334159(v=exchg.10).md">Itag</a></span><span class="sxs-lookup"><span data-stu-id="e618d-134"><a href="dn334159(v=exchg.10).md">Itag</a></span></span></td>
<td><span data-ttu-id="e618d-135">Obtient ou définit le ITAG de la colonne.</span><span class="sxs-lookup"><span data-stu-id="e618d-135">Gets or sets the itag of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e618d-137"><a href="dn334205(v=exchg.10).md">Durée</a></span><span class="sxs-lookup"><span data-stu-id="e618d-137"><a href="dn334205(v=exchg.10).md">Length</a></span></span></td>
<td><span data-ttu-id="e618d-138">Obtient la longueur actuelle du flux.</span><span class="sxs-lookup"><span data-stu-id="e618d-138">Gets the current length of the stream.</span></span> <span data-ttu-id="e618d-139">(Substitue <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream. Length</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-139">(Overrides <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream.Length</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e618d-141"><a href="dn334161(v=exchg.10).md">Position</a></span><span class="sxs-lookup"><span data-stu-id="e618d-141"><a href="dn334161(v=exchg.10).md">Position</a></span></span></td>
<td><span data-ttu-id="e618d-142">Obtient ou définit la position actuelle dans le flux.</span><span class="sxs-lookup"><span data-stu-id="e618d-142">Gets or sets the current position in the stream.</span></span> <span data-ttu-id="e618d-143">(Substitue <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream. position</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-143">(Overrides <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream.Position</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e618d-145"><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></span><span class="sxs-lookup"><span data-stu-id="e618d-145"><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></span></span></td>
<td><span data-ttu-id="e618d-146">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-146">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e618d-148"><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></span><span class="sxs-lookup"><span data-stu-id="e618d-148"><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></span></span></td>
<td><span data-ttu-id="e618d-149">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-149">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e618d-150">Haut</span><span class="sxs-lookup"><span data-stu-id="e618d-150">Top</span></span>

## <a name="methods"></a><span data-ttu-id="e618d-151">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e618d-151">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e618d-152">Nom</span><span class="sxs-lookup"><span data-stu-id="e618d-152">Name</span></span></th>
<th><span data-ttu-id="e618d-153">Description</span><span class="sxs-lookup"><span data-stu-id="e618d-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-155"><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></span><span class="sxs-lookup"><span data-stu-id="e618d-155"><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></span></span></td>
<td><span data-ttu-id="e618d-156">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-156">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-158"><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></span><span class="sxs-lookup"><span data-stu-id="e618d-158"><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></span></span></td>
<td><span data-ttu-id="e618d-159">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-159">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-161"><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Fermer</a></span><span class="sxs-lookup"><span data-stu-id="e618d-161"><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Close</a></span></span></td>
<td><span data-ttu-id="e618d-162">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-162">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-164"><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></span><span class="sxs-lookup"><span data-stu-id="e618d-164"><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></span></span></td>
<td><span data-ttu-id="e618d-165">(Héritée de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-165">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="e618d-167"><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></span><span class="sxs-lookup"><span data-stu-id="e618d-167"><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></span></span></td>
<td><span data-ttu-id="e618d-168"><strong>Obsolète.</strong></span><span class="sxs-lookup"><span data-stu-id="e618d-168"><strong>Obsolete.</strong></span></span> <span data-ttu-id="e618d-169">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-169">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-171"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="e618d-171"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose()</a></span></span></td>
<td><span data-ttu-id="e618d-172">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-172">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="e618d-174"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose (booléen)</a></span><span class="sxs-lookup"><span data-stu-id="e618d-174"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="e618d-175">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-175">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-177"><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></span><span class="sxs-lookup"><span data-stu-id="e618d-177"><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></span></span></td>
<td><span data-ttu-id="e618d-178">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-178">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-180"><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></span><span class="sxs-lookup"><span data-stu-id="e618d-180"><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></span></span></td>
<td><span data-ttu-id="e618d-181">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-181">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-183"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="e618d-183"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="e618d-184">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-184">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="e618d-186"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="e618d-186"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="e618d-187">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-187">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-189"><a href="dn334193(v=exchg.10).md">Purge</a></span><span class="sxs-lookup"><span data-stu-id="e618d-189"><a href="dn334193(v=exchg.10).md">Flush</a></span></span></td>
<td><span data-ttu-id="e618d-190">Videz le flux.</span><span class="sxs-lookup"><span data-stu-id="e618d-190">Flush the stream.</span></span> <span data-ttu-id="e618d-191">(Substitue <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream. Flush ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-191">(Overrides <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream.Flush()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-193"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="e618d-193"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="e618d-194">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-194">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-196"><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></span><span class="sxs-lookup"><span data-stu-id="e618d-196"><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></span></span></td>
<td><span data-ttu-id="e618d-197">(Héritée de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-197">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-199"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="e618d-199"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="e618d-200">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-200">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-202"><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></span><span class="sxs-lookup"><span data-stu-id="e618d-202"><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></span></span></td>
<td><span data-ttu-id="e618d-203">(Héritée de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-203">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="e618d-205"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone ()</a></span><span class="sxs-lookup"><span data-stu-id="e618d-205"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone()</a></span></span></td>
<td><span data-ttu-id="e618d-206">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-206">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="e618d-208"><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone (booléen)</a></span><span class="sxs-lookup"><span data-stu-id="e618d-208"><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone(Boolean)</a></span></span></td>
<td><span data-ttu-id="e618d-209">(Héritée de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-209">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-211"><a href="dn334198(v=exchg.10).md">Lire</a></span><span class="sxs-lookup"><span data-stu-id="e618d-211"><a href="dn334198(v=exchg.10).md">Read</a></span></span></td>
<td><span data-ttu-id="e618d-212">Lit une séquence d'octets dans le flux actuel et avance la position dans le flux du nombre d'octets lus.</span><span class="sxs-lookup"><span data-stu-id="e618d-212">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span> <span data-ttu-id="e618d-213">(Substitue <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream. Read ([], Int32, Int32)</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-213">(Overrides <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream.Read([], Int32, Int32)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-215"><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></span><span class="sxs-lookup"><span data-stu-id="e618d-215"><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></span></span></td>
<td><span data-ttu-id="e618d-216">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-216">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-218"><a href="dn334154(v=exchg.10).md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="e618d-218"><a href="dn334154(v=exchg.10).md">Seek</a></span></span></td>
<td><span data-ttu-id="e618d-219">Définit la position dans le flux actuel.</span><span class="sxs-lookup"><span data-stu-id="e618d-219">Sets the position in the current stream.</span></span> <span data-ttu-id="e618d-220">(Substitue <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">Stream. Seek (Int64, SeekOrigin)</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-220">(Overrides <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">Stream.Seek(Int64, SeekOrigin)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-222"><a href="dn334196(v=exchg.10).md">SetLength</a></span><span class="sxs-lookup"><span data-stu-id="e618d-222"><a href="dn334196(v=exchg.10).md">SetLength</a></span></span></td>
<td><span data-ttu-id="e618d-223">Définit la longueur du flux.</span><span class="sxs-lookup"><span data-stu-id="e618d-223">Sets the length of the stream.</span></span> <span data-ttu-id="e618d-224">(Substitue <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream. SetLength (Int64)</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-224">(Overrides <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream.SetLength(Int64)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-226"><a href="dn334149(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="e618d-226"><a href="dn334149(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="e618d-227">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente le <a href="dn334143(v=exchg.10).md">ColumnStream</a>actuel.</span><span class="sxs-lookup"><span data-stu-id="e618d-227">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn334143(v=exchg.10).md">ColumnStream</a>.</span></span> <span data-ttu-id="e618d-228">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-228">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-230"><a href="dn334197(v=exchg.10).md">Écrire</a></span><span class="sxs-lookup"><span data-stu-id="e618d-230"><a href="dn334197(v=exchg.10).md">Write</a></span></span></td>
<td><span data-ttu-id="e618d-231">Écrit une séquence d’octets dans le flux actuel et avance la position actuelle dans ce flux du nombre d’octets écrits.</span><span class="sxs-lookup"><span data-stu-id="e618d-231">Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written.</span></span> <span data-ttu-id="e618d-232">(Substitue <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">Stream. Write ([], Int32, Int32)</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-232">(Overrides <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">Stream.Write([], Int32, Int32)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e618d-234"><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></span><span class="sxs-lookup"><span data-stu-id="e618d-234"><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></span></span></td>
<td><span data-ttu-id="e618d-235">(Héritée de <a href="/dotnet/api/system.io.stream">Stream</a>.)</span><span class="sxs-lookup"><span data-stu-id="e618d-235">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e618d-236">Haut</span><span class="sxs-lookup"><span data-stu-id="e618d-236">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="e618d-237">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e618d-237">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e618d-238">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e618d-238">Reference</span></span>

[<span data-ttu-id="e618d-239">ColumnStream, classe</span><span class="sxs-lookup"><span data-stu-id="e618d-239">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="e618d-240">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e618d-240">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
