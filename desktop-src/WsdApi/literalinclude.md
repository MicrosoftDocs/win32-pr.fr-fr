---
description: Place une instruction include C ou IDL dans le code généré.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: élément literalInclude
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1f43f1b8d3d95e2ad8a378dd1c8cbada7758ad
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995126"
---
# <a name="literalinclude-element"></a>élément literalInclude

Place une instruction include C ou IDL dans le code généré.

## <a name="usage"></a>Usage

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Type</th>
<th>Obligatoire</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Langage</strong><br/></td>
<td>chaîne de langue<br/></td>
<td>Non<br/></td>
<td>Type de fichier d’en-tête à inclure. <br/> <br/>
<dt><strong>Secteur</strong></dt> <dd> Incluez un fichier d’en-tête C.<br/> </dd> <dt><strong>MIDL</strong></dt> <dd> Incluez un fichier IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Local</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Cet attribut est utilisé uniquement lorsque la <strong>langue</strong> est définie sur &quot; C &quot; .<br/> <br/>
<dt><strong>:</strong></dt> <dd> Recherche l’en-tête nommé dans le répertoire actif avant de rechercher dans les répertoires système.<br/> </dd> <dt><strong>Fausses</strong></dt> <dd> Recherche uniquement les répertoires système pour l’en-tête nommé.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**txt**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="remarks"></a>Remarques

Les exemples suivants illustrent le code généré à partir de différents éléments **literalInclude** .

### <a name="example-1---generating-a-c-include-statement"></a>Exemple 1 : génération d’une instruction include C

XML d’entrée :

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

Code de sortie :

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a>Exemple 2 : génération d’une instruction include C

XML d’entrée :

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

Code de sortie :

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a>Exemple 3 : génération d’une instruction d’importation IDL

XML d’entrée :

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

Code de sortie :

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




