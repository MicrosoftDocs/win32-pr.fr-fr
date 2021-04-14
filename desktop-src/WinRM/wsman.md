---
title: Objet WSMan (WSManDisp. h)
description: Fournit des méthodes et des propriétés utilisées pour créer une session, représentée par un objet de session.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- Objet WSMan Windows Remote Management
- Objet WSMan Windows Remote Management, Description
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384003"
---
# <a name="wsman-object"></a><span data-ttu-id="01aa7-105">Objet WSMan</span><span class="sxs-lookup"><span data-stu-id="01aa7-105">WSMan object</span></span>

<span data-ttu-id="01aa7-106">Fournit des méthodes et des propriétés utilisées pour créer une session, représentée par un objet de [**session**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="01aa7-106">Provides methods and properties used to create a session, represented by a [**Session**](session.md) object.</span></span> <span data-ttu-id="01aa7-107">Toute opération de Windows Remote Management nécessite la création d’une [**session**](session.md) qui se connecte à un ordinateur distant, à un [*contrôleur de gestion de base*](windows-remote-management-glossary.md) (BMC) ou à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="01aa7-107">Any Windows Remote Management operations require creation of a [**Session**](session.md) that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="01aa7-108">Les opérations incluent l’obtention, l’écriture, l’énumération de données ou l’appel de méthodes.</span><span class="sxs-lookup"><span data-stu-id="01aa7-108">Operations include getting, writing, enumerating data, or invoking methods.</span></span>

## <a name="members"></a><span data-ttu-id="01aa7-109">Membres</span><span class="sxs-lookup"><span data-stu-id="01aa7-109">Members</span></span>

<span data-ttu-id="01aa7-110">L’objet **WSMan** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="01aa7-110">The **WSMan** object has these types of members:</span></span>

-   [<span data-ttu-id="01aa7-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="01aa7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="01aa7-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="01aa7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="01aa7-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="01aa7-113">Methods</span></span>

<span data-ttu-id="01aa7-114">L’objet **WSMan** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="01aa7-114">The **WSMan** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="01aa7-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="01aa7-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="01aa7-116">Description</span><span class="sxs-lookup"><span data-stu-id="01aa7-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01aa7-117"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-117"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-118">Crée un objet <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> qui spécifie le nom d’utilisateur et le mot de passe utilisés lors de la création d’une session à distance.</span><span class="sxs-lookup"><span data-stu-id="01aa7-118">Creates a <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> object that specifies the user name and password used when creating a remote session.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="01aa7-119"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-119"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-120">Crée un objet <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> qui peut spécifier les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="01aa7-120">Creates a <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> object that can specify:</span></span><br/>
<ul>
<li><span data-ttu-id="01aa7-121">Le chemin d’accès complet à une <a href="windows-remote-management-glossary.md"><em>ressource</em></a> ou à un élément de données unique.</span><span class="sxs-lookup"><span data-stu-id="01aa7-121">The complete path to a <a href="windows-remote-management-glossary.md"><em>resource</em></a> or a single piece of data.</span></span></li>
<li><span data-ttu-id="01aa7-122"><a href="windows-remote-management-glossary.md"><em>Sélecteur</em></a> pour une instance spécifique d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="01aa7-122">A <a href="windows-remote-management-glossary.md"><em>selector</em></a> for a specific instance of a resource.</span></span></li>
<li><span data-ttu-id="01aa7-123"><a href="windows-remote-management-glossary.md"><em>Option</em></a> qui fournit des données supplémentaires au fournisseur de ressources.</span><span class="sxs-lookup"><span data-stu-id="01aa7-123">An <a href="windows-remote-management-glossary.md"><em>option</em></a> that supplies additional data to the resource provider.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01aa7-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-125">Crée un objet de <a href="session.md"><strong>session</strong></a> qui peut ensuite être utilisé pour les opérations réseau ultérieures.</span><span class="sxs-lookup"><span data-stu-id="01aa7-125">Creates a <a href="session.md"><strong>Session</strong></a> object that can then be used for subsequent network operations.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="01aa7-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan. EnumerationFlagHierarchyDeep</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan.EnumerationFlagHierarchyDeep</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-127">Retourne la valeur de l’indicateur d’énumération <strong>EnumerationFlagHierarchyDeep</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="session-enumerate.md"><strong>session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-127">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeep</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01aa7-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan. EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan.EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-129">Retourne la valeur de l’indicateur d’énumération <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="session-enumerate.md"><strong>session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-129">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="01aa7-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan. EnumerationFlagHierarchyShallow</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan.EnumerationFlagHierarchyShallow</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-131">Retourne la valeur de l’indicateur d’énumération <strong>EnumerationFlagHierarchyShallow</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="session-enumerate.md"><strong>session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-131">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyShallow</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01aa7-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan. EnumerationFlagNonXmlText</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan.EnumerationFlagNonXmlText</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-133">Retourne la valeur de la constante d’énumération <strong>WSManFlagNonXmlText</strong> à utiliser dans le paramètre <em>Flags</em> de la méthode <a href="session-enumerate.md"><strong>session. Enumerate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="01aa7-133">Returns the value of the enumeration constant <strong>WSManFlagNonXmlText</strong> for use in the <em>flags</em> parameter of the <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="01aa7-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan. EnumerationFlagReturnEPR</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan.EnumerationFlagReturnEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-135">Retourne la valeur de l’indicateur d’énumération <strong>EnumerationFlagReturnEPR</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="session-enumerate.md"><strong>session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-135">Returns the value of the enumeration flag <strong>EnumerationFlagReturnEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01aa7-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan. EnumerationFlagReturnObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan.EnumerationFlagReturnObject</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-137">Retourne la valeur de l’indicateur d’énumération <strong>EnumerationFlagReturnObject</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="session-enumerate.md"><strong>session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-137">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObject</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="01aa7-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan. EnumerationFlagReturnObjectAndEPR</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan.EnumerationFlagReturnObjectAndEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-139">Retourne la valeur de l’indicateur d’énumération <strong>EnumerationFlagReturnObjectAndEPR</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="session-enumerate.md"><strong>session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-139">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObjectAndEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01aa7-140"><a href="wsman-geterrormessage.md"><strong>WSMan. GetErrorMessage</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-140"><a href="wsman-geterrormessage.md"><strong>WSMan.GetErrorMessage</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-141">Retourne une chaîne mise en forme contenant le texte d’un numéro d’erreur.</span><span class="sxs-lookup"><span data-stu-id="01aa7-141">Returns a formatted string containing the text of an error number.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="01aa7-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan. SessionFlagCredUsernamePassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan.SessionFlagCredUsernamePassword</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-143">Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagCredUsernamePassword</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-143">Returns the value of the authentication flag <strong>WSManFlagCredUsernamePassword</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01aa7-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan. SessionFlagEnableSPNServerPort</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan.SessionFlagEnableSPNServerPort</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-145">Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagEnableSPNServerPort</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-145">Returns the value of the authentication flag <strong>WSManFlagEnableSPNServerPort</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="01aa7-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan. SessionFlagNoEncryption</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan.SessionFlagNoEncryption</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-147">Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagNoEncryption</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-147">Returns the value of the authentication flag <strong>WSManFlagNoEncryption</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01aa7-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan. SessionFlagSkipCACheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan.SessionFlagSkipCACheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-149">Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagSkipCACheck</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-149">Returns the value of the <strong>WSManFlagSkipCACheck</strong> authentication flag for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="01aa7-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan. SessionFlagSkipCNCheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan.SessionFlagSkipCNCheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-151">Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagSkipCNCheck</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-151">Returns the value of the authentication flag <strong>WSManFlagSkipCNCheck</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01aa7-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan. SessionFlagUseBasic</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan.SessionFlagUseBasic</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-153">Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagUseBasic</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-153">Returns the value of the authentication flag <strong>WSManFlagUseBasic</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="01aa7-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan. SessionFlagUseDigest</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan.SessionFlagUseDigest</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-155">Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagUseDigest</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-155">Returns the value of the authentication flag <strong>WSManFlagUseDigest</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01aa7-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan. SessionFlagUseKerberos</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan.SessionFlagUseKerberos</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-157">Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagUseKerberos</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-157">Returns the value of the authentication flag <strong>WSManFlagUseKerberos</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="01aa7-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan. SessionFlagUseNegotiate</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan.SessionFlagUseNegotiate</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-159">Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagUseNegotiate</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-159">Returns the value of the authentication flag <strong>WSManFlagUseNegotiate</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="01aa7-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan. SessionFlagUseNoAuthentication</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan.SessionFlagUseNoAuthentication</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-161">Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagUseNoAuthentication</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-161">Returns the value of the authentication flag <strong>WSManFlagUseNoAuthentication</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="01aa7-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan. SessionFlagUTF8</strong></a></span><span class="sxs-lookup"><span data-stu-id="01aa7-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan.SessionFlagUTF8</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="01aa7-163">Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagUTF8</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="01aa7-163">Returns the value of the authentication flag <strong>WSManFlagUTF8</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="01aa7-164">Propriétés</span><span class="sxs-lookup"><span data-stu-id="01aa7-164">Properties</span></span>

<span data-ttu-id="01aa7-165">L’objet **WSMan** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="01aa7-165">The **WSMan** object has these properties.</span></span>



| <span data-ttu-id="01aa7-166">Propriété</span><span class="sxs-lookup"><span data-stu-id="01aa7-166">Property</span></span>                                            | <span data-ttu-id="01aa7-167">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="01aa7-167">Access type</span></span>          | <span data-ttu-id="01aa7-168">Description</span><span class="sxs-lookup"><span data-stu-id="01aa7-168">Description</span></span>                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="01aa7-169">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="01aa7-169">**CommandLine**</span></span>](wsman-commandline.md)<br/> | <span data-ttu-id="01aa7-170">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01aa7-170">Read-only</span></span><br/> | <span data-ttu-id="01aa7-171">Obtient la ligne de commande non traités pour le processus d’hébergement actuel.</span><span class="sxs-lookup"><span data-stu-id="01aa7-171">Gets the unprocessed command line for the current hosting process.</span></span><br/> |
| [<span data-ttu-id="01aa7-172">**Error**</span><span class="sxs-lookup"><span data-stu-id="01aa7-172">**Error**</span></span>](wsman-error.md)<br/>             | <span data-ttu-id="01aa7-173">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="01aa7-173">Read-only</span></span><br/> | <span data-ttu-id="01aa7-174">Obtient les informations d’erreur.</span><span class="sxs-lookup"><span data-stu-id="01aa7-174">Gets error information.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="01aa7-175">Notes</span><span class="sxs-lookup"><span data-stu-id="01aa7-175">Remarks</span></span>

<span data-ttu-id="01aa7-176">L’objet **WSMan** correspond aux interfaces [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) et [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) .</span><span class="sxs-lookup"><span data-stu-id="01aa7-176">The **WSMan** object corresponds to the [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) interfaces.</span></span> <span data-ttu-id="01aa7-177">**WSMan** est le seul objet qui peut être créé directement à l’aide de [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="01aa7-177">**WSMan** is the only object that can be created directly using [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="01aa7-178">Exemples</span><span class="sxs-lookup"><span data-stu-id="01aa7-178">Examples</span></span>

<span data-ttu-id="01aa7-179">L’exemple de code suivant montre comment instancier un objet **WSMan** .</span><span class="sxs-lookup"><span data-stu-id="01aa7-179">The following code example shows how to instantiate a **WSMan** object.</span></span>


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a><span data-ttu-id="01aa7-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01aa7-180">Requirements</span></span>



| <span data-ttu-id="01aa7-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01aa7-181">Requirement</span></span> | <span data-ttu-id="01aa7-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="01aa7-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01aa7-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01aa7-183">Minimum supported client</span></span><br/> | <span data-ttu-id="01aa7-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01aa7-184">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="01aa7-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01aa7-185">Minimum supported server</span></span><br/> | <span data-ttu-id="01aa7-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01aa7-186">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="01aa7-187">En-tête</span><span class="sxs-lookup"><span data-stu-id="01aa7-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="01aa7-188"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="01aa7-188"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="01aa7-189">MIDL</span><span class="sxs-lookup"><span data-stu-id="01aa7-189">IDL</span></span><br/>                      | <dl> <span data-ttu-id="01aa7-190"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01aa7-190"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="01aa7-191">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01aa7-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="01aa7-192"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="01aa7-192"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="01aa7-193">DLL</span><span class="sxs-lookup"><span data-stu-id="01aa7-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01aa7-194"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01aa7-194"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01aa7-195">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01aa7-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01aa7-196">API de script WinRM</span><span class="sxs-lookup"><span data-stu-id="01aa7-196">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="01aa7-197">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="01aa7-197">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="01aa7-198">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="01aa7-198">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="01aa7-199">Scripts dans Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="01aa7-199">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="01aa7-200">Obtention de données à partir de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="01aa7-200">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="01aa7-201">Obtention de données à partir d’un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="01aa7-201">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

