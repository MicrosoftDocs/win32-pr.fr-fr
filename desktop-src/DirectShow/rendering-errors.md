---
description: Erreurs de rendu
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Erreurs de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31d49c5fbb82457282decdaa07152e75db6bc3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312298"
---
# <a name="rendering-errors"></a>Erreurs de rendu

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

Microsoft® DirectShow® (DES) définit différents codes d’erreur utilisés pour consigner les erreurs de rendu. Si un projet ne s’affiche pas correctement, le moteur de rendu appelle la méthode [**IAMErrorLog :: LogError**](iamerrorlog-logerror.md) . Le tableau suivant récapitule les paramètres fournis à **LogError**:

-   Le code d’erreur est contenu dans le paramètre *ErrorCode* .
-   La description est contenue dans le paramètre ErrorString.
-   La description est contenue dans le paramètre *ErrorString* .
-   S’il existe des informations supplémentaires, le type **Variant** est contenu dans le membre **VT** de la **variante** vers laquelle pointe *pExtraInfo*.

> [!Note]  
> Les codes d’erreur décrits ici ne sont pas des valeurs **HRESULT** . Pour obtenir la liste des valeurs de retour **HRESULT** spécifiques à des, consultez [codes d’erreur et de réussite](error-and-success-codes.md).

 




| Code d'erreur | Description | Informations supplémentaires | Type de variante | 
|------------|-------------|-------------------|--------------|
| DEX_IDS_BAD_SOURCE_NAME | le nom de fichier n’existe pas ou DirectShow ne reconnaît pas l’extension de fichier. | Nom de fichier | <strong>BSTR</strong> | 
| DEX_IDS_BAD_SOURCE_NAME2 | Le type de fichier ne correspond pas à l’extension de fichier ou le fichier est endommagé. | Nom de fichier | <strong>BSTR</strong> | 
| DEX_IDS_MISSING_SOURCE_NAME | Le nom de fichier est requis, mais n’a pas été donné. | None | Non applicable | 
| DEX_IDS_UNKNOWN_SOURCE | Impossible d’analyser la source de données fournie par cette source. | None | Non applicable | 
| DEX_IDS_INSTALL_PROBLEM | Erreur inattendue. certains DirectShow composant ne sont pas installés correctement. | None | Non applicable | 
| DEX_IDS_NO_SOURCE_NAMES | Le filtre source n’accepte pas les noms de fichiers. | None | Non applicable | 
| DEX_IDS_BAD_MEDIATYPE | Le type de média du groupe n’est pas pris en charge. | Numéro du groupe | <strong>int</strong> | 
| DEX_IDS_STREAM_NUMBER | Numéro de flux non valide pour cette source. | Numéro de flux | <strong>int</strong> | 
| DEX_IDS_OUTOFMEMORY | Mémoire insuffisante. | None | Non applicable | 
| DEX_IDS_DIBSEQ_NOTALLSAME | Une image bitmap de la séquence n’est pas du même type que les autres. | Nom de la bitmap | <strong>BSTR</strong> | 
| DEX_IDS_CLIPTOOSHORT | Les heures de média du clip ne sont pas valides ou la séquence de bitmaps indépendantes du périphérique (DIB) est trop petite.<blockquote>[!Note]<br />Si d’autres erreurs de rendu se produisent, cette erreur peut se produire même si les temps de support sont valides.</blockquote><br /> | None | Non applicable | 
| DEX_IDS_INVALID_DXT | L’identificateur de classe (CLSID) de l’effet ou de la transition n’est pas valide. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_INVALID_DEFAULT_DXT | Le CLSID de l’effet ou de la transition par défaut n’est pas valide. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_NO_3D | Votre version de DirectX ne prend pas en charge les transitions en trois dimensions. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_BROKEN_DXT | Cet effet n’est pas le bon type ou est rompu. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_NO_SUCH_PROPERTY | Aucune propriété de ce type n’existe sur l’objet. | Nom de la propriété | <strong>BSTR</strong> | 
| DEX_IDS_ILLEGAL_PROPERTY_VAL | Valeur non conforme pour cette propriété. | Valeur spécifiée | <strong>DIFFÉRENT</strong> | 
| DEX_IDS_INVALID_XML | Erreur de syntaxe dans le fichier XML. | Numéro de ligne | VT_I4 (entier sur 4 octets) | 
| DEX_IDS_CANT_FIND_FILTER | Le filtre spécifié dans XML est introuvable par catégorie et par instance. | Nom convivial (instance) | <strong>BSTR</strong> | 
| DEX_IDS_DISK_WRITE_ERROR | Erreur lors de l’écriture du fichier XML sur le disque. | None | Non applicable | 
| DEX_IDS_INVALID_AUDIO_FX | CLSID n’est pas un filtre d’effet audio DirectShow valide. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_CANT_FIND_COMPRESSOR | Impossible de trouver un compresseur pour produire le format de compression spécifié. | None | Non applicable | 




 

Les erreurs suivantes ne doivent jamais se produire. Si vous rencontrez l’une de ces erreurs, veuillez envoyer un rapport de bogue à Microsoft.



| Code d'erreur                 | Description                                 |
|----------------------------|---------------------------------------------|
| analyse de la \_ chronologie des ID DEX \_ \_  | Erreur inattendue lors de l’analyse de la chronologie.      |
| \_Erreur du \_ graphique des ID DEX \_     | Erreur inattendue lors de la génération du graphique de filtre. |
| \_erreur de \_ grille \_ ID DEX      | Erreur inattendue avec la grille interne.    |
| erreur de l' \_ interface ID DEX \_ \_ | Erreur inattendue lors de l’obtention d’une interface.      |



 

 

 




