---
title: Jeux de propriétés DocumentSummaryInformation et UserDefined
description: Un jeu de propriétés DocumentSummaryInformation et UserDefined est une extension du jeu de propriétés d’informations de résumé. Les deux jeux de propriétés peuvent exister simultanément.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- Jeux de propriétés UserDefined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237251"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a>Jeux de propriétés DocumentSummaryInformation et UserDefined

Un jeu de propriétés **DocumentSummaryInformation** et **UserDefined** est une extension [du jeu de propriétés d’informations de résumé](the-summary-information-property-set.md). Les deux jeux de propriétés peuvent exister simultanément.

Le nom du flux qui contient le jeu de propriétés **DocumentSummaryInformation** est **« \\ 005DocumentSummaryInformation »**. L’identificateur de format (FMTID) pour le jeu de propriétés **DocumentSummaryInformation** est **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.

La déclaration de cette valeur est disponible dans les fichiers d’en-tête fournis sous la forme **fmtid \_ DocSummaryInformation**. Pour plus d’informations, consultez [noms dans IStorage](names-in-istorage.md), [propriété informations de synthèse définie](the-summary-information-property-set.md), [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) et [format identificateurs](format-identifiers.md).

Ce flux comporte également une section distincte pour les propriétés personnalisées définies par l’utilisateur, comme dans les jeux de propriétés **DocumentSummaryInformation** et **UserDefined** . Cette section apparaît dans l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) en tant que jeu de propriétés distinct, avec le fmtid suivant (disponible en tant que **fmtid \_ UserDefinedProperties**) : **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.

Ces deux jeux de propriétés sont les seuls pour lesquels un seul flux peut contenir plusieurs jeux de propriétés. Le fait que ces deux jeux de propriétés se trouvent dans un seul flux affecte le comportement de l’interface **IPropertySetStorage** . Pour plus d’informations, consultez [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).

Le tableau suivant répertorie les propriétés ajoutées au jeu de propriétés **DocumentSummaryInformation** et **UserDefined** . Comme dans le jeu de propriétés **SummaryInformation** , les noms ne sont généralement pas stockés dans le jeu de propriétés, mais sont déduits à partir de l’identificateur de propriété.



| Nom de la propriété      | Identificateur de propriété     | Valeur de l’identificateur de propriété | Type VARIANT                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| Category           | **\_catégorie PIDDSI**    | 0x00000002                | **VT- \_ LPSTR**                     |
| PresentationTarget | **PIDDSI \_ PRESFORMAT**  | 0x00000003                | **VT- \_ LPSTR**                     |
| Octets              | **PIDDSI \_ BYTECOUNT**   | 0x00000004                | **VT \_**                        |
| Lignes              | **PIDDSI \_ LINECOUNT**   | 0x00000005                | **VT \_**                        |
| Paragraphes         | **PIDDSI \_ PARCOUNT**    | 0x00000006                | **VT \_**                        |
| Diapositives             | **PIDDSI \_ SLIDECOUNT**  | 0x00000007                | **VT \_**                        |
| Notes              | **PIDDSI \_ NOTECOUNT**   | 0x00000008                | **VT \_**                        |
| HiddenSlides       | **PIDDSI \_ HIDDENCOUNT** | 0x00000009                | **VT \_**                        |
| MMClips            | **PIDDSI \_ MMCLIPCOUNT** | Stop                | **VT \_**                        |
| ScaleCrop          | **\_échelle PIDDSI**       | 0x0000000B                | **VT \_ bool**                      |
| HeadingPairs       | **PIDDSI \_ HEADINGPAIR** | 0x0000000C                | **VT \_** \| **\_ vecteur VT** de variante |
| TitlesofParts      | **PIDDSI \_ DOCPARTS**    | 0x0000000D                | **VT \_ vecteur** \| **VT \_ LPSTR**   |
| Manager            | **\_Gestionnaire PIDDSI**     | 0x0000000E                | **VT- \_ LPSTR**                     |
| Company            | **\_entreprise PIDDSI**     | 0x0000000F                | **VT- \_ LPSTR**                     |
| LinksUpToDate      | **PIDDSI \_ LINKSDIRTY**  | 0x00000010                | **VT \_ bool**                      |



 

Ces propriétés ont les utilisations suivantes :

<dl> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Catégorie
</dt> <dd>

Chaîne de texte tapée par l’utilisateur qui indique la catégorie à laquelle le fichier appartient (Mémo, proposition, etc.). Il est utile pour rechercher des fichiers du même type.

</dd> <dt>

<span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget
</dt> <dd>

Format cible pour la présentation (35mm, imprimante, vidéo, etc.).

</dd> <dt>

<span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bits
</dt> <dd>

Nombre d'octets.

</dd> <dt>

<span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Courbes
</dt> <dd>

Nombre de lignes.

</dd> <dt>

<span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Suivants
</dt> <dd>

Nombre de paragraphes.

</dd> <dt>

<span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Suivantes
</dt> <dd>

Nombre de diapositives.

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Notes
</dt> <dd>

Nombre de pages qui contiennent des remarques.

</dd> <dt>

<span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides
</dt> <dd>

Nombre de diapositives masquées.

</dd> <dt>

<span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips
</dt> <dd>

Nombre de clips audio ou vidéo.

</dd> <dt>

<span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop
</dt> <dd>

Affectez la valeur true (-1) lorsque la mise à l’échelle de la miniature est souhaitée. Si la valeur n’est pas définie, le rognage est souhaité.

</dd> <dt>

<span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs
</dt> <dd>

Propriété utilisée en interne indiquant le regroupement de différentes parties de document et le nombre d’éléments dans chaque groupe. Les titres des parties de document sont stockés dans la propriété **TitlesofParts** . La propriété **HeadingPairs** est stockée sous la forme d’un vecteur de variantes, dans des paires répétées de valeurs **VT \_ LPSTR** (ou **VT \_ LPWStr**) et **VT \_ I4** . La valeur de **VT \_ LPSTR** représente un nom de titre et la valeur **VT \_ I4** indique le nombre de parties de document sous cet en-tête.

</dd> <dt>

<span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts
</dt> <dd>

Noms des parties de document.

</dd> <dt>

<span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Gestion
</dt> <dd>

Gestionnaire du projet.

</dd> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Entreprise
</dt> <dd>

Nom de la société

</dd> <dt>

<span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate
</dt> <dd>

Valeur booléenne pour indiquer si les liens personnalisés sont gênés par un bruit excessif, pour toutes les applications.

> [!Note]  
> Comme décrit dans 12,3. Format sérialisé pour les jeux de propriétés de la spécification de conception OLE 2,0, les éléments vectoriels dans les propriétés **HeadingPairs** et **TitlesofParts** doivent être alignés sur des limites de 32 bits dans le jeu de propriétés. Toutefois, dans les jeux de propriétés **DocumentSummaryInformation** et **UserDefined** , lorsque la page de codes du jeu de propriétés n’est pas Unicode, ces éléments doivent être empaquetés.

 

</dd> </dl>

La propriété **UserDefined** définie peut être utilisée pour contenir toutes les propriétés. En règle générale, il est utilisé pour stocker les propriétés nommées créées par un utilisateur.

 

 




