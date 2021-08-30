---
description: 'En savoir plus sur : membres d’instance'
title: Membres d’instance
TOCTitle: Instance members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance_members(v=EXCHG.10)
ms:contentKeyID: 55103299
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f1b3b533c7893385902cad41e1300105995e7b389c61776c47e17341817bbac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093859"
---
# <a name="instance-members"></a>Membres d’instance

Inclure les membres protégés  
Inclure les membres hérités  

Classe qui encapsule un [JET_INSTANCE](./jet-instance-structure.md) dans un objet jetable. L’instance doit être fermée en dernier et la fermeture de l’instance libère toutes les autres ressources pour l’instance.

Le type d' [instance](./instance-class.md) expose les membres suivants.

## <a name="constructors"></a>Constructeurs

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn350924(v=exchg.10).md">Instance (String)</a></td>
<td>Initialise une nouvelle instance de la classe d’instance. Le JET_INSTANCE sous-jacent est alloué, mais pas initialisé.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn350927(v=exchg.10).md">Instance (String, String)</a></td>
<td>Initialise une nouvelle instance de la classe d’instance. Le JET_INSTANCE sous-jacent est alloué, mais pas initialisé.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn350948(v=exchg.10).md">Instance (String, String, TermGrbit)</a></td>
<td>Initialise une nouvelle instance de la classe d’instance. Le JET_INSTANCE sous-jacent est alloué, mais pas initialisé.</td>
</tr>
</tbody>
</table>


Haut

## <a name="properties"></a>Propriétés

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></td>
<td>(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">IsInvalid</a></td>
<td>(Héritée de <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350941(v=exchg.10).md">JetInstance</a></td>
<td>Obtient le JET_INSTANCE contenu dans cette instance.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350962(v=exchg.10).md">Paramètres</a></td>
<td>Obtient le InstanceParameters pour cette instance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn350964(v=exchg.10).md">TermGrbit</a></td>
<td>Obtient ou définit le TermGrbit pour cette instance.</td>
</tr>
</tbody>
</table>


Haut

## <a name="methods"></a>Méthodes

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Fermer</a></td>
<td>(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">DangerousAddRef</a></td>
<td>(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></td>
<td>(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></td>
<td>(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Dispose ()</a></td>
<td>(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Dispose (booléen)</a></td>
<td>(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finaliser</a></td>
<td>(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn350932(v=exchg.10).md">Init ()</a></td>
<td>Initialisez le JET_INSTANCE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn350954(v=exchg.10).md">Init (InitGrbit)</a></td>
<td>Initialisez le JET_INSTANCE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn350934(v=exchg.10).md">Init (JET_RSTINFO, InitGrbit)</a></td>
<td>Initialisez le JET_INSTANCE. Cette API nécessite au moins la version Vista d’ESENT.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></td>
<td>Libère le handle pour cette instance. (Substitue <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle. ReleaseHandle ()</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">SetHandle</a></td>
<td>(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">SetHandleAsInvalid</a></td>
<td>(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn350935(v=exchg.10).md">Terme</a></td>
<td>Terminez le JET_INSTANCE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn350960(v=exchg.10).md">ToString</a></td>
<td>Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente l' <a href="dn350923(v=exchg.10).md">instance</a>actuelle. (Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Haut

## <a name="operators"></a>Opérateurs

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn350950(v=exchg.10).md">Implicite (instance to JET_INSTANCE)</a></td>
<td>Fournir la conversion implicite d’un objet d’instance en une structure JET_INSTANCE. Cette opération est effectuée afin qu’une instance puisse être utilisée partout où une JET_INSTANCE est requise.</td>
</tr>
</tbody>
</table>


Haut

## <a name="fields"></a>Champs

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.protfield(exchg.10).gif" title="Champ protégé" alt="Protected field" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">traitée</a></td>
<td>(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’instance](./instance-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
