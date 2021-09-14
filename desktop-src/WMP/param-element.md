---
title: PARAM, élément (kit de développement logiciel (SDK) WMP)
description: L’élément PARAM définit un paramètre personnalisé associé à une sélection ou à un élément d’une sélection.
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- PARAM, élément Lecteur Windows Media
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918963"
---
# <a name="param-element"></a>Élément PARAM

L’élément **param** définit un paramètre personnalisé associé à une sélection ou à un élément d’une sélection.

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a>Paramètres

Un paramètre peut également être associé à l’affichage plutôt qu’à un élément individuel, en plaçant cet élément directement après la balise **ASX** . Ces éléments sont référencés par leurs noms et une valeur d’index commençant par zéro.

> [!Note]  
> cet élément **ASX** est disponible uniquement pour Lecteur Windows Media version 6,01 et versions ultérieures. l’installation standard de Microsoft Internet Explorer 5 comprend une version compatible de Lecteur Windows Media.

 

## <a name="attributes"></a>Attributs

**NAME**

Nom utilisé pour accéder à la valeur du paramètre. Le nom peut être n’importe quelle chaîne valide. Les chaînes suivantes ont déjà été définies.



| String                          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowShuffle                    | l’attribut **VALUE** spécifie si la sélection de métafichier permet à la fonctionnalité de lecture aléatoire Lecteur Windows Media de lire les entrées dans un ordre aléatoire. L’attribut value peut avoir la **valeur** « Yes » ou « no ». La valeur par défaut est « no ».                                                                                                                                                                                                                                                                                                                                                                  |
| CanPause                        | L’attribut **value** spécifie si l’utilisateur peut suspendre la lecture. L’attribut value peut avoir la **valeur** « Yes » ou « no ». La valeur par défaut est « Yes ».                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CanSeek                         | L’attribut **value** spécifie si l’utilisateur peut modifier la position de lecture actuelle à l’aide de la barre de recherche, de l’avance rapide ou de l’inverse rapide. L’attribut value peut avoir la **valeur** « Yes » ou « no ». La valeur par défaut est « Yes ».                                                                                                                                                                                                                                                                                                                                                                    |
| CanSkipBack                     | L’attribut **value** spécifie si l’utilisateur peut revenir à l’élément de sélection précédent en cliquant sur **précédent**. L’attribut value peut avoir la **valeur** « Yes » ou « no ». La valeur par défaut est « Yes ».                                                                                                                                                                                                                                                                                                                                                                                         |
| CanSkipForward                  | L’attribut **value** spécifie si l’utilisateur peut avancer jusqu’à l’élément de sélection suivant en cliquant sur **suivant**. L’attribut value peut avoir la **valeur** « Yes » ou « no ». La valeur par défaut est « Yes ».                                                                                                                                                                                                                                                                                                                                                                                                  |
| CPRadioID                       | L’attribut **value** spécifie l’ID d’un flux radio fourni par un magasin en ligne de type 1. Autrement dit, l’attribut **value** doit être égal au champ RadioID de l’un des flux radio dans le catalogue du magasin en ligne. L’élément parent est l’élément **ASX** .                                                                                                                                                                                                                                                                                                                                   |
| Encodage                        | L’attribut **value** est défini sur « UTF-8 » pour indiquer que le métafichier est un fichier encodé en Unicode (UTF-8).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| HtmlFlink                       | L’attribut **value** est une chaîne fournie par un magasin de type 1 en ligne. Lecteur Windows Media transmet la chaîne à la méthode [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , qui est implémentée par le plug-in du magasin en ligne. La méthode **GetItemInfo** retourne l’URL de la page Web à afficher dans le volet de **lecture à présent** du lecteur. La page Web a accès à toutes les méthodes que l’objet **externe** expose aux magasins de type 1. Pour obtenir la liste de ces méthodes, consultez [objet externe pour les magasins de type 1 en ligne](external-object-for-type-1-online-stores.md). |
| HTMLView                        | L’attribut **value** spécifie une URL qui s’affiche dans le volet de **lecture à présent** du lecteur en mode complet pendant la durée de la sélection ou l’entrée actuelle selon que l’élément parent est l’élément **ASX** ou un élément d' **entrée** . HTMLView n’est pas pris en charge pour le contrôle Lecteur Windows Media.                                                                                                                                                                                                                                                                               |
| JRN :*fieldName* \[ :*espace de noms*\] | L’attribut **value** spécifie la valeur dans laquelle le champ de journal indiqué sera défini. La partie :*namespace* de l’attribut **Name** est facultative.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Prémémoire tampon                       | L’attribut **value** spécifie si l’entrée de playlist suivante commence la mise en mémoire tampon avant la fin de l’entrée actuelle, ce qui permet une transition transparente. L’attribut value peut avoir la **valeur** « true » ou « false ».                                                                                                                                                                                                                                                                                                                                                                                 |
| ShowWhileBuffering              | L’attribut **value** spécifie si un fichier image référencé par l’élément d' **entrée** actuel continue à s’afficher au-delà de la durée spécifiée pendant la mise en mémoire tampon de l’entrée de playlist suivante. L’attribut value peut avoir la **valeur** « true » ou « false ».                                                                                                                                                                                                                                                                                                                                         |



 

**VALUE**

Valeur associée à ce paramètre. Il peut s’agir d’une valeur numérique ou de chaîne.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments           |
|-----------------|--------------------|
| Éléments parents | **ASX**, **entrée** |
| Éléments enfants  | None               |



 

## <a name="remarks"></a>Notes

Cet élément permet aux utilisateurs de placer des informations supplémentaires sur chaque clip à l’intérieur de l’élément d' **entrée** qui le contient. Pour récupérer les informations de métadonnées spécifiées dans l' **entrée** de la playlist, utilisez le *support*. méthode **getItemInfo** . *Média*. la méthode **getItemInfo** récupère la valeur de l’attribut **value** , en fonction du nom du paramètre. les versions précédentes de Lecteur Windows Media récupérer les informations de métadonnées spécifiées dans l' **entrée** de la playlist, à l’aide de la méthode **GetMediaParameter** en fonction du nom du paramètre et d’un numéro d’index pour l’entrée.

Un paramètre peut également être associé à l’affichage plutôt qu’à un élément individuel, en plaçant cet élément directement après la balise **ASX** . Ces éléments sont référencés par leurs noms et une valeur d’index commençant par zéro.

**Remarque**

cet élément **ASX** est disponible uniquement pour Lecteur Windows Media version 6,01 et versions ultérieures. l’installation standard de Microsoft Internet Explorer 5 comprend une version compatible de Lecteur Windows Media.

## <a name="examples"></a>Exemples


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure, Lecteur Windows Media série 9 ou version ultérieure est requise pour les attributs de nom prédéfinis, Lecteur Windows Media 10 ou version ultérieure est requis pour les noms prédéfinis CanPause, CanSeek, CanSkipBack et CanSkipForward<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**affichage des Pages Web dans les Lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Journalisation des données de flux**](logging-stream-data.md)
</dt> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





