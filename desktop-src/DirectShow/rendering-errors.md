---
description: Erreurs de rendu
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Erreurs de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482233"
---
# <a name="rendering-errors"></a>Erreurs de rendu

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

Microsoft® DirectShow® Editing services (DES) définit différents codes d’erreur utilisés pour consigner les erreurs de rendu. Si un projet ne s’affiche pas correctement, le moteur de rendu appelle la méthode [**IAMErrorLog :: LogError**](iamerrorlog-logerror.md) . Le tableau suivant récapitule les paramètres fournis à **LogError**:

-   Le code d’erreur est contenu dans le paramètre *ErrorCode* .
-   La description est contenue dans le paramètre ErrorString.
-   La description est contenue dans le paramètre *ErrorString* .
-   S’il existe des informations supplémentaires, le type **Variant** est contenu dans le membre **VT** de la **variante** vers laquelle pointe *pExtraInfo*.

> [!Note]  
> Les codes d’erreur décrits ici ne sont pas des valeurs **HRESULT** . Pour obtenir la liste des valeurs de retour **HRESULT** spécifiques à des, consultez [codes d’erreur et de réussite](error-and-success-codes.md).

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Code d'erreur</th>
<th>Description</th>
<th>Informations supplémentaires</th>
<th>Type de variante</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DEX_IDS_BAD_SOURCE_NAME</td>
<td>Le nom de fichier n’existe pas ou DirectShow ne reconnaît pas l’extension de fichier.</td>
<td>Nom de fichier</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_BAD_SOURCE_NAME2</td>
<td>Le type de fichier ne correspond pas à l’extension de fichier ou le fichier est endommagé.</td>
<td>Nom de fichier</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_MISSING_SOURCE_NAME</td>
<td>Le nom de fichier est requis, mais n’a pas été donné.</td>
<td>Aucune</td>
<td>Non applicable</td>
</tr>
<tr class="even">
<td>DEX_IDS_UNKNOWN_SOURCE</td>
<td>Impossible d’analyser la source de données fournie par cette source.</td>
<td>Aucune</td>
<td>Non applicable</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INSTALL_PROBLEM</td>
<td>Erreur inattendue. Certains composants DirectShow ne sont pas installés correctement.</td>
<td>Aucune</td>
<td>Non applicable</td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SOURCE_NAMES</td>
<td>Le filtre source n’accepte pas les noms de fichiers.</td>
<td>Aucune</td>
<td>Non applicable</td>
</tr>
<tr class="odd">
<td>DEX_IDS_BAD_MEDIATYPE</td>
<td>Le type de média du groupe n’est pas pris en charge.</td>
<td>Numéro du groupe</td>
<td><strong>int</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_STREAM_NUMBER</td>
<td>Numéro de flux non valide pour cette source.</td>
<td>Numéro de flux</td>
<td><strong>int</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_OUTOFMEMORY</td>
<td>Mémoire insuffisante.</td>
<td>Aucune</td>
<td>Non applicable</td>
</tr>
<tr class="even">
<td>DEX_IDS_DIBSEQ_NOTALLSAME</td>
<td>Une image bitmap de la séquence n’est pas du même type que les autres.</td>
<td>Nom de la bitmap</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_CLIPTOOSHORT</td>
<td>Les heures de média du clip ne sont pas valides ou la séquence de bitmaps indépendantes du périphérique (DIB) est trop petite.
<blockquote>
[!Note]<br />
Si d’autres erreurs de rendu se produisent, cette erreur peut se produire même si les temps de support sont valides.
</blockquote>
<br/></td>
<td>Aucune</td>
<td>Non applicable</td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_DXT</td>
<td>L’identificateur de classe (CLSID) de l’effet ou de la transition n’est pas valide.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_DEFAULT_DXT</td>
<td>Le CLSID de l’effet ou de la transition par défaut n’est pas valide.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_3D</td>
<td>Votre version de DirectX ne prend pas en charge les transitions en trois dimensions.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_BROKEN_DXT</td>
<td>Cet effet n’est pas le bon type ou est rompu.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SUCH_PROPERTY</td>
<td>Aucune propriété de ce type n’existe sur l’objet.</td>
<td>Nom de la propriété</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_ILLEGAL_PROPERTY_VAL</td>
<td>Valeur non conforme pour cette propriété.</td>
<td>Valeur spécifiée</td>
<td><strong>DIFFÉRENT</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_XML</td>
<td>Erreur de syntaxe dans le fichier XML.</td>
<td>Numéro de ligne</td>
<td>VT_I4 (entier sur 4 octets)</td>
</tr>
<tr class="odd">
<td>DEX_IDS_CANT_FIND_FILTER</td>
<td>Le filtre spécifié dans XML est introuvable par catégorie et par instance.</td>
<td>Nom convivial (instance)</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_DISK_WRITE_ERROR</td>
<td>Erreur lors de l’écriture du fichier XML sur le disque.</td>
<td>Aucune</td>
<td>Non applicable</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_AUDIO_FX</td>
<td>CLSID n’est pas un filtre d’effet audio DirectShow valide.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_CANT_FIND_COMPRESSOR</td>
<td>Impossible de trouver un compresseur pour produire le format de compression spécifié.</td>
<td>Aucune</td>
<td>Non applicable</td>
</tr>
</tbody>
</table>



 

Les erreurs suivantes ne doivent jamais se produire. Si vous rencontrez l’une de ces erreurs, veuillez envoyer un rapport de bogue à Microsoft.



| Code d'erreur                 | Description                                 |
|----------------------------|---------------------------------------------|
| analyse de la \_ chronologie des ID DEX \_ \_  | Erreur inattendue lors de l’analyse de la chronologie.      |
| \_Erreur du \_ graphique des ID DEX \_     | Erreur inattendue lors de la génération du graphique de filtre. |
| \_erreur de \_ grille \_ ID DEX      | Erreur inattendue avec la grille interne.    |
| erreur de l' \_ interface ID DEX \_ \_ | Erreur inattendue lors de l’obtention d’une interface.      |



 

 

 




