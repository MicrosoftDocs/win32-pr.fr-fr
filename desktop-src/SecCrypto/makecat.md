---
description: Outil CryptoAPI qui crée un fichier de catalogue.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980c58530c55006d28ecd7589b0313844e9dbe46
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886254"
---
# <a name="makecat"></a>MakeCat

L’outil MakeCat est un outil CryptoAPI qui crée un fichier de catalogue. MakeCat est disponible dans le cadre du kit de développement logiciel (SDK) de Microsoft Windows pour Windows 7 et .NET Framework 4,0 et est installé, par défaut, dans le \\ dossier Bin du chemin d’installation du kit de développement logiciel (sdk).

L’outil MakeCat utilise la syntaxe de commande suivante :

**MakeCat** \[ **-n** \| **-r** \| **-v** \] *Nom du fichier*

## <a name="parameters"></a>Paramètres



| Paramètre             | Description                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-n**<br/>     | Ne s’arrête pas sur une erreur récupérable.<br/>                                                                                                                           |
| **-r**<br/>     | Force MakeCat à se terminer s’il rencontre des erreurs récupérables. Plus précisément, il se termine lors du traitement des entrées dans la section des fichiers de catalogue d’un fichier. CDF.<br/> |
| **-v**<br/>     | Verbose. Affiche tous les messages de progression et d’erreur.<br/>                                                                                                            |
| *FileName*<br/> | Nom du fichier. CDF à analyser. Pour connaître la structure et le contenu requis, consultez la section Notes.<br/>                                                                         |



 

## <a name="remarks"></a>Remarques

Le fichier. CDF doit être généré avec les spécifications suivantes.

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> La dernière entrée dans le fichier. CDF doit toujours avoir un caractère de saut de ligne explicite à la fin de la ligne.

 

La \[ \] section CatalogHeader définit des informations sur l’ensemble du fichier catalogue.



| Option                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom<br/>           | Nom du fichier catalogue, y compris son extension.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ResultDir<br/>      | Répertoire dans lequel le fichier. cat créé sera placé. Si ce paramètre n’est pas indiqué, le répertoire actif par défaut est utilisé. Si le répertoire n’existe pas, il est créé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PublicVersion<br/>  | Cette option n'est pas prise en charge. <br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Version du catalogue. Si le champ n’est pas renseigné, la valeur par défaut, 1, est utilisée.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| CatalogVersion<br/> | Version du catalogue. Si la version n’est pas présente ou a la valeur 1, « 0x100 » est passé au paramètre *dwPublicVersion* de la fonction [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) et un fichier catalogue de la version 1 est créé. L’option HashAlgorithms doit être vide ou contenir SHA1.<br/> Si la version est définie sur 2, « 0x200 » est passé au paramètre *dwPublicVersion* de la fonction [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) et un fichier catalogue de la version 2 est créé. L’option HashAlgorithms doit contenir SHA256.<br/> Si cette option est présente mais contient une valeur autre que 1 ou 2, l’outil MakeCat génère une erreur.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette option n’est pas prise en charge.<br/> <br/> |
| HashAlgorithms<br/> | Nom de l’algorithme de hachage utilisé. Pour plus d’informations, consultez l’option CatalogVersion.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette option n’est pas prise en charge.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PageHashes<br/>     | Spécifie s’il faut hacher les fichiers listés dans l' &lt; &gt; option HASH dans la \[ \] section CatalogFiles<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette option n’est pas prise en charge.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| EncodingType<br/>   | Type d’encodage de message utilisé. Si le champ n’est pas renseigné, la valeur par défaut de EncodingType est PKCS \_ 7 \_ ASN \_ Encoding \| x509 \_ ASN \_ , 0x00010001. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

La \[ \] section CatalogFiles définit chaque membre du fichier catalogue avec des fichiers de types différents et des attributs de différents types dans des groupes distincts.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>balise de référence<br/></td>
<td>Référence de texte au fichier. Il peut s’agir de caractères de texte ASCII, à l’exception du signe égal (=). Le système doit être en mesure de reproduire cette balise après l’installation. <br/> Utilisez &lt; hash &gt; comme préfixe du nom de fichier. La balise est alors le hachage du fichier sous forme de chaîne ASCII. <br/></td>
</tr>
<tr class="even">
<td>nom et chemin d’accès du fichier<br/></td>
<td>Nom du fichier, y compris l’extension à analyser et le chemin d’accès relatif au fichier. Tout type de fichier pouvant être signé avec SignTool peut être ajouté à un catalogue. Par exemple, les noms de fichiers avec les extensions suivantes, entre autres, peuvent être ajoutés à un catalogue : .exe, .cab,. cat,. ocx, .dll et. STL.<br/></td>
</tr>
<tr class="odd">
<td>ALTSIPID<br/></td>
<td>GUID SIP qui doit être utilisé pour le hachage au lieu du SIP standard en fonction du type de fichier. Cette entrée est facultative. Si cette entrée est omise, le membre sera haché à l’aide du SIP par défaut. Si aucun SIP installé par défaut n’est trouvé, le SIP plat sera utilisé.<br/></td>
</tr>
<tr class="even">
<td>guid<br/></td>
<td>Représentation textuelle d’un GUID.<br/></td>
</tr>
<tr class="odd">
<td>ATTRx<br/></td>
<td>Facultatif. Attribut ou instruction sur le fichier ou le contenu. Il peut y avoir un nombre quelconque d’attributs, y compris aucun.<br/></td>
</tr>
<tr class="even">
<td>type<br/></td>
<td>Définit le type d’attribut qui est ajouté au format 0x00000000 (texte). Cette option peut être<strong>une combinaison or au niveau</strong> du bit de zéro ou plusieurs des valeurs suivantes :<br/>
<ul>
<li>0x10000000 attribut authentifié (signé, inclus dans le hachage).</li>
<li>0x20000000 attribut non authentifié (non signé, non inclus dans le hachage, non vérifiable).</li>
<li>l’attribut 0x01000000 n’est pas répliqué sur les entrées SHA1 dans un catalogue CatalogVersion 2.</li>
<li>l’attribut 0x00010000 est représenté en texte brut. Aucune conversion n’est effectuée.</li>
<li>l’attribut 0x00020000 est représenté dans l’encodage de base 64. Utilisé pour représenter des données binaires.</li>
<li>l’attribut 0x00000001 est une paire nom-valeur. Utilisez l’option OID pour le nom. Cet attribut est lent ; par conséquent, utilisez cette option avec modération.</li>
<li>l’attribut 0x00000002 est référencé par un <a href="/windows/desktop/SecGloss/o-gly"><em>identificateur d’objet</em></a> (OID).</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>oid<br/></td>
<td>Représentation textuelle de la clé de référence de l’attribut. Il s’agit d’un OID sous la forme d’une chaîne de texte en notation à quatre points (par exemple, a. b. c. d) ou d’un nom de texte.<br/></td>
</tr>
<tr class="even">
<td>value<br/></td>
<td>Représentation textuelle de la valeur de l’attribut. Le type de représentation textuelle utilisé dépend de la valeur de l’option type. Les caractères EOL déterminent la longueur.<br/></td>
</tr>
<tr class="odd">
<td>&lt;FORMAT&gt;<br/></td>
<td>Hache le fichier spécifié.<br/></td>
</tr>
</tbody>
</table>



 

Le fichier catalogue généré n’est pas signé. S’il doit être signé avant de transmettre, il est signé à l’aide de [SignTool](signtool.md).

 

 
