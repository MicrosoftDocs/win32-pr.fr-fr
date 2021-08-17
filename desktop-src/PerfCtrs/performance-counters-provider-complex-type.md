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
ms.openlocfilehash: 4470754e710faf9f7abe5a94cfb2e08e6e79c1b0415110b96dbac35807556911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061066"
---
# <a name="provider-complex-type"></a>Type complexe du fournisseur

Définit un fournisseur et les compteurs qu’il fournit.

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

## <a name="child-elements"></a>Éléments enfants



| Élément        | Type                                                                   | Description                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **counterSet** | [**Man : counterSet**](performance-counters-counterset-complex-type.md) | Identifie l’ensemble de compteurs qui contient un ou plusieurs compteurs logiquement liés.<br/> |



## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>applicationIdentity</td>
<td><strong>xs:string</strong></td>
<td>Nom du fichier binaire qui contient les chaînes de ressources localisées, soit un fichier .exe, soit .dll (n’incluez pas le chemin d’accès au fichier binaire).<br/> L’utilitaire Lodctr.exe utilise le chemin d’accès à partir du paramètre facultatif [<em>path</em>] pour rechercher le fichier binaire. Par exemple, <strong>lodctr</strong> [<strong>/m :</strong><em>Manifest</em> [<em>chemin</em>]]. Si vous n’incluez pas le paramètre [<em>path</em>], Lodctr.exe recherche le dossier qui contient le manifeste.<br/></td>
</tr>
<tr class="even">
<td>rappel</td>

<td>Cet attribut indique que vous souhaitez recevoir une notification lorsqu’un consommateur effectue certaines actions. <br/> Si vous incluez cet attribut, l’outil CTRPP utilise la signature de fonction <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> de remplacement, que vous utilisez pour passer le nom de votre fonction qui implémente la fonction de rappel <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> .<br/> En guise d’alternative à la spécification de cet attribut, vous pouvez utiliser l’argument <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> .<br/> <strong>Windows Vista :</strong> La seule valeur valide pour cet attribut est &quot; Custom &quot; . L’utilitaire <a href="ctrpp.md">CTRPP</a> génère le modèle pour une fonction de rappel <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> . Le modèle est inclus dans le fichier. c que CTRPP a généré. <br/> <br/></td>
</tr>
<tr class="odd">
<td>providerGuid</td>
<td><a href="performance-counters-guidtype-simple-type.md"><strong>homme : GUIDType</strong></a></td>
<td>GUID de chaîne qui identifie de façon unique le fournisseur dans le manifeste. Le GUID doit être unique dans le manifeste.<br/> Vous devez fournir un nouveau GUID uniquement lorsque la version de l’application change (si vous prenez en charge les installations côte à côte).<br/></td>
</tr>
<tr class="even">
<td>providerName</td>
<td><strong>xs:string</strong></td>
<td>Nom utilisé pour créer le nom de la classe de Win32_PerfRawData WMI. Si vous ne spécifiez pas de nom, &quot; &quot; les compteurs sont utilisés comme nom de la classe.<br/></td>
</tr>
<tr class="odd">
<td>providerType</td>

<td>Indique si le fournisseur est un fournisseur en mode utilisateur, un fournisseur en mode noyau ou un fournisseur de pilotes. Les valeurs possibles sont les suivantes.<br/> 
<table>
<thead>
<tr class="header">
<th>Terme</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode<br/></td>
<td>Spécifiez ce mode pour un composant en mode utilisateur, tel qu’une application, une DLL ou un pilote en mode utilisateur. Les extensions types pour les composants en mode utilisateur sont .exe ou .dll. Il s’agit de la valeur par défaut.<br/></td>
</tr>
<tr class="even">
<td><span id="kernel"></span><span id="KERNEL"></span>noyau<br/></td>
<td>Spécifiez ce mode pour un composant en mode noyau, tel qu’un pilote WDM ou WDF. L’extension classique des composants en mode noyau est .sys.<br/> <strong>Windows Vista et Windows Server 2008 :</strong> cette valeur n’est pas prise en charge tant que Windows 7 et Windows Server 2008 R2.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>resourceBase</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>homme : UInt32Type</strong></a></td>
<td><p>Définit la valeur initiale de l’index de ressource utilisée par <a href="ctrpp.md">CTRPP</a> pour générer les identificateurs de ressource.</p></td>
</tr>
<tr class="odd">
<td>symbole</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>homme : CSymbolType</strong></a></td>
<td><p>Nom symbolique qui identifie le fournisseur. L’outil <a href="ctrpp.md">CTRPP</a> crée une variable de handle que vous pouvez utiliser lors de l’appel de fonctions qui requièrent un handle pour le fournisseur (par exemple, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>). Le nom symbolique est le nom de la variable.</p>
<p>Si vous incluez l’argument <strong>-prefix</strong> lors de l’appel de <a href="ctrpp.md">CTRPP</a>, la chaîne de préfixe est ajoutée au début du nom symbolique.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




