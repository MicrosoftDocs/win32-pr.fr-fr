---
description: Définit un fournisseur et les compteurs qu’il fournit.
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: Type complexe du fournisseur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eec52139710d0ffafe06f22504a735e59312818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865097"
---
# <a name="provider-complex-type"></a><span data-ttu-id="7ba99-103">Type complexe du fournisseur</span><span class="sxs-lookup"><span data-stu-id="7ba99-103">provider Complex Type</span></span>

<span data-ttu-id="7ba99-104">Définit un fournisseur et les compteurs qu’il fournit.</span><span class="sxs-lookup"><span data-stu-id="7ba99-104">Defines a provider and the counters that it provides.</span></span>

``` syntax
<xs:complexType name="provider">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="counterSet"
            type="man:counterSet"
        >
            <xs:key name="uniqueCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@id"
                 />
            </xs:key>
            <xs:unique name="uniqueCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:unique>
            <xs:keyref name="existBaseID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@baseID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfTimeID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfTimeID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfFreqID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfFreqID"
                 />
            </xs:keyref>
            <xs:keyref name="existMultiCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@multiCounterID"
                 />
            </xs:keyref>
            <xs:key name="uniqueStructNames">
                <xs:selector
                    xpath="./man:structs/man:struct"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
            <xs:keyref name="existCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@struct"
                 />
            </xs:keyref>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="callback"
        use="optional"
        default="default"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="custom"
                 />
                <xs:enumeration
                    value="default"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerGuid"
        type="man:GUIDType"
        use="required"
     />
    <xs:attribute name="applicationIdentity"
        type="xs:string"
        use="required"
     />
    <xs:attribute name="providerType"
        use="optional"
        default="userMode"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="userMode"
                 />
                <xs:enumeration
                    value="kernelMode"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerName"
        type="xs:string"
        use="optional"
        default="Counters"
     />
    <xs:attribute name="resourceBase"
        type="man:UInt32Type"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7ba99-105">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7ba99-105">Child elements</span></span>



| <span data-ttu-id="7ba99-106">Élément</span><span class="sxs-lookup"><span data-stu-id="7ba99-106">Element</span></span>        | <span data-ttu-id="7ba99-107">Type</span><span class="sxs-lookup"><span data-stu-id="7ba99-107">Type</span></span>                                                                   | <span data-ttu-id="7ba99-108">Description</span><span class="sxs-lookup"><span data-stu-id="7ba99-108">Description</span></span>                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba99-109">**counterSet**</span><span class="sxs-lookup"><span data-stu-id="7ba99-109">**counterSet**</span></span> | [<span data-ttu-id="7ba99-110">**Man : counterSet**</span><span class="sxs-lookup"><span data-stu-id="7ba99-110">**man:counterSet**</span></span>](performance-counters-counterset-complex-type.md) | <span data-ttu-id="7ba99-111">Identifie l’ensemble de compteurs qui contient un ou plusieurs compteurs logiquement liés.</span><span class="sxs-lookup"><span data-stu-id="7ba99-111">Identifies the counter set that contains one or more logically related counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="7ba99-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="7ba99-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ba99-113">Nom</span><span class="sxs-lookup"><span data-stu-id="7ba99-113">Name</span></span></th>
<th><span data-ttu-id="7ba99-114">Type</span><span class="sxs-lookup"><span data-stu-id="7ba99-114">Type</span></span></th>
<th><span data-ttu-id="7ba99-115">Description</span><span class="sxs-lookup"><span data-stu-id="7ba99-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ba99-116">applicationIdentity</span><span class="sxs-lookup"><span data-stu-id="7ba99-116">applicationIdentity</span></span></td>
<td><span data-ttu-id="7ba99-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="7ba99-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="7ba99-118">Nom du fichier binaire qui contient les chaînes de ressources localisées, soit un fichier. exe, soit un fichier. dll (n’incluez pas le chemin d’accès au fichier binaire).</span><span class="sxs-lookup"><span data-stu-id="7ba99-118">The name of the binary file that contains the localized resource strings, either an .exe or .dll file (do not include the path to the binary).</span></span><br/> <span data-ttu-id="7ba99-119">L’utilitaire Lodctr.exe utilise le chemin d’accès à partir du paramètre facultatif [<em>path</em>] pour rechercher le fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="7ba99-119">The Lodctr.exe utility uses the path from the optional [<em>path</em>] parameter to search for the binary file.</span></span> <span data-ttu-id="7ba99-120">Par exemple, <strong>lodctr</strong> [<strong>/m :</strong><em>Manifest</em> [<em>chemin</em>]].</span><span class="sxs-lookup"><span data-stu-id="7ba99-120">For example, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>path</em>]].</span></span> <span data-ttu-id="7ba99-121">Si vous n’incluez pas le paramètre [<em>path</em>], Lodctr.exe recherche le dossier qui contient le manifeste.</span><span class="sxs-lookup"><span data-stu-id="7ba99-121">If you do not include the [<em>path</em>] parameter, Lodctr.exe searches the folder that contains the manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ba99-122">rappel</span><span class="sxs-lookup"><span data-stu-id="7ba99-122">callback</span></span></td>

<td><span data-ttu-id="7ba99-123">Cet attribut indique que vous souhaitez recevoir une notification lorsqu’un consommateur effectue certaines actions.</span><span class="sxs-lookup"><span data-stu-id="7ba99-123">This attribute indicates that you want to receive notification when a consumer performs certain actions.</span></span> <br/> <span data-ttu-id="7ba99-124">Si vous incluez cet attribut, l’outil CTRPP utilise la signature de fonction <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> de remplacement, que vous utilisez pour passer le nom de votre fonction qui implémente la fonction de rappel <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7ba99-124">If you include this attribute, the CTRPP tool uses the alternate <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> function signature, which you use to pass in the name of your function that implements the <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span><br/> <span data-ttu-id="7ba99-125">En guise d’alternative à la spécification de cet attribut, vous pouvez utiliser l’argument <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> .</span><span class="sxs-lookup"><span data-stu-id="7ba99-125">As an alternative to specifying this attribute, you can use the <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> argument.</span></span><br/> <span data-ttu-id="7ba99-126"><strong>Windows Vista :</strong> La seule valeur valide pour cet attribut est &quot; Custom &quot; .</span><span class="sxs-lookup"><span data-stu-id="7ba99-126"><strong>Windows Vista:</strong> The only valid value for this attribute is &quot;custom&quot;.</span></span> <span data-ttu-id="7ba99-127">L’utilitaire <a href="ctrpp.md">CTRPP</a> génère le modèle pour une fonction de rappel <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7ba99-127">The <a href="ctrpp.md">CTRPP</a> utility generates the template for a <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span> <span data-ttu-id="7ba99-128">Le modèle est inclus dans le fichier. c que CTRPP a généré.</span><span class="sxs-lookup"><span data-stu-id="7ba99-128">The template is included in the .c file that CTRPP generated.</span></span> <br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ba99-129">providerGuid</span><span class="sxs-lookup"><span data-stu-id="7ba99-129">providerGuid</span></span></td>
<td><span data-ttu-id="7ba99-130"><a href="performance-counters-guidtype-simple-type.md"><strong>homme : GUIDType</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ba99-130"><a href="performance-counters-guidtype-simple-type.md"><strong>man:GUIDType</strong></a></span></span></td>
<td><span data-ttu-id="7ba99-131">GUID de chaîne qui identifie de façon unique le fournisseur dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="7ba99-131">String GUID that uniquely identifies the provider in the manifest.</span></span> <span data-ttu-id="7ba99-132">Le GUID doit être unique dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="7ba99-132">The GUID must be unique within the manifest.</span></span><br/> <span data-ttu-id="7ba99-133">Vous devez fournir un nouveau GUID uniquement lorsque la version de l’application change (si vous prenez en charge les installations côte à côte).</span><span class="sxs-lookup"><span data-stu-id="7ba99-133">You need to provide a new GUID only when the version of the application changes (if you support side-by-side installations).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ba99-134">providerName</span><span class="sxs-lookup"><span data-stu-id="7ba99-134">providerName</span></span></td>
<td><span data-ttu-id="7ba99-135"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="7ba99-135"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="7ba99-136">Nom utilisé pour créer le nom de la classe de Win32_PerfRawData WMI.</span><span class="sxs-lookup"><span data-stu-id="7ba99-136">The name that is used to create the WMI Win32_PerfRawData class name.</span></span> <span data-ttu-id="7ba99-137">Si vous ne spécifiez pas de nom, &quot; &quot; les compteurs sont utilisés comme nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="7ba99-137">If you do not specify a name, &quot;Counters&quot; is used as the name of the class.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ba99-138">providerType</span><span class="sxs-lookup"><span data-stu-id="7ba99-138">providerType</span></span></td>

<td><span data-ttu-id="7ba99-139">Indique si le fournisseur est un fournisseur en mode utilisateur, un fournisseur en mode noyau ou un fournisseur de pilotes.</span><span class="sxs-lookup"><span data-stu-id="7ba99-139">Identifies whether the provider is a user-mode provider, kernel-mode provider, or driver provider.</span></span> <span data-ttu-id="7ba99-140">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="7ba99-140">Possible values are as follows.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7ba99-141">Terme</span><span class="sxs-lookup"><span data-stu-id="7ba99-141">Term</span></span></th>
<th><span data-ttu-id="7ba99-142">Description</span><span class="sxs-lookup"><span data-stu-id="7ba99-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ba99-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode</span><span class="sxs-lookup"><span data-stu-id="7ba99-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode</span></span><br/></td>
<td><span data-ttu-id="7ba99-144">Spécifiez ce mode pour un composant en mode utilisateur, tel qu’une application, une DLL ou un pilote en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ba99-144">Specify this mode for a user-mode component such as an application, a DLL, or a user-mode driver.</span></span> <span data-ttu-id="7ba99-145">Les extensions classiques pour les composants en mode utilisateur sont. exe ou. dll.</span><span class="sxs-lookup"><span data-stu-id="7ba99-145">The typical extensions for user-mode components are .exe or .dll.</span></span> <span data-ttu-id="7ba99-146">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ba99-146">This is the default.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ba99-147"><span id="kernel"></span><span id="KERNEL"></span>noyau</span><span class="sxs-lookup"><span data-stu-id="7ba99-147"><span id="kernel"></span><span id="KERNEL"></span>kernel</span></span><br/></td>
<td><span data-ttu-id="7ba99-148">Spécifiez ce mode pour un composant en mode noyau, tel qu’un pilote WDM ou WDF.</span><span class="sxs-lookup"><span data-stu-id="7ba99-148">Specify this mode for a kernel-mode component such as a WDM or WDF driver.</span></span> <span data-ttu-id="7ba99-149">L’extension classique des composants en mode noyau est. sys.</span><span class="sxs-lookup"><span data-stu-id="7ba99-149">The typical extension for kernel-mode components is .sys.</span></span><br/> <span data-ttu-id="7ba99-150"><strong>Windows Vista et Windows Server 2008 :</strong> Cette valeur n’est pas prise en charge avant Windows 7 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="7ba99-150"><strong>Windows Vista and Windows Server 2008:</strong> This value is not supported until Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ba99-151">resourceBase</span><span class="sxs-lookup"><span data-stu-id="7ba99-151">resourceBase</span></span></td>
<td><span data-ttu-id="7ba99-152"><a href="performance-counters-uint32type-simple-type.md"><strong>homme : UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ba99-152"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><p><span data-ttu-id="7ba99-153">Définit la valeur initiale de l’index de ressource utilisée par <a href="ctrpp.md">CTRPP</a> pour générer les identificateurs de ressource.</span><span class="sxs-lookup"><span data-stu-id="7ba99-153">Defines the starting resource index value that <a href="ctrpp.md">CTRPP</a> uses to generate the resource identifiers.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ba99-154">symbole</span><span class="sxs-lookup"><span data-stu-id="7ba99-154">symbol</span></span></td>
<td><span data-ttu-id="7ba99-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>homme : CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="7ba99-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="7ba99-156">Nom symbolique qui identifie le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7ba99-156">A symbolic name that identifies the provider.</span></span> <span data-ttu-id="7ba99-157">L’outil <a href="ctrpp.md">CTRPP</a> crée une variable de handle que vous pouvez utiliser lors de l’appel de fonctions qui requièrent un handle pour le fournisseur (par exemple, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="7ba99-157">The <a href="ctrpp.md">CTRPP</a> tool creates a HANDLE variable that you can use when calling functions that require a handle to the provider (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>).</span></span> <span data-ttu-id="7ba99-158">Le nom symbolique est le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="7ba99-158">The symbolic name is the name of the variable.</span></span></p>
<p><span data-ttu-id="7ba99-159">Si vous incluez l’argument <strong>-prefix</strong> lors de l’appel de <a href="ctrpp.md">CTRPP</a>, la chaîne de préfixe est ajoutée au début du nom symbolique.</span><span class="sxs-lookup"><span data-stu-id="7ba99-159">If you include the <strong>-prefix</strong> argument when calling <a href="ctrpp.md">CTRPP</a>, the prefix string is added to the beginning of the symbolic name.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="7ba99-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ba99-160">Requirements</span></span>



| <span data-ttu-id="7ba99-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ba99-161">Requirement</span></span> | <span data-ttu-id="7ba99-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ba99-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ba99-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ba99-163">Minimum supported client</span></span><br/> | <span data-ttu-id="7ba99-164">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ba99-164">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7ba99-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ba99-165">Minimum supported server</span></span><br/> | <span data-ttu-id="7ba99-166">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ba99-166">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




