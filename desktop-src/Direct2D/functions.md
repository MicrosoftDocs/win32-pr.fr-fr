---
title: Fonctions Direct2D
description: Direct2D fournit les fonctions suivantes.
ms.assetid: 1a7ae962-9b70-442c-a676-f172a2d9bfd3
keywords:
- Direct2D, fonctions
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 9cbe07a6c1054036030395ff965610919ee48a97
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104463898"
---
# <a name="direct2d-functions"></a>Fonctions Direct2D

Direct2D fournit les fonctions suivantes. Des fonctions supplémentaires sont définies dans l' [espace de noms d2d1](d2d1-namespace.md).

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**D2D1ComputeMaximumScaleFactor**](/windows/desktop/api/d2d1_2/nf-d2d1_2-d2d1computemaximumscalefactor) | Calcule le facteur maximal par lequel une transformation donnée peut étirer n’importe quel vecteur. |
| [**D2D1CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) | Crée un appareil Direct2D associé à l’appareil DXGI fourni.  |
| [**D2D1CreateDeviceContext**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevicecontext) | Crée un contexte de périphérique Direct2D associé à une surface DXGI.  |
| [**D2D1CreateFactory (D2D1_FACTORY_TYPE, REFIID, void \* \* )**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory-r1) | Crée un objet de fabrique qui peut être utilisé pour créer des ressources Direct2D. |
| [**D2D1CreateFactory (D2D1_FACTORY_TYPE, REFIID, D2D1_FACTORY_OPTIONS \* , void \* \* )**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) | Crée un objet de fabrique qui peut être utilisé pour créer des ressources Direct2D. |
| [**D2D1GetGradientMeshInteriorPointsFromCoonsPatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-d2d1getgradientmeshinteriorpointsfromcoonspatch) | Retourne les points intérieurs d’un correctif de maillage dégradé en fonction des points définissant un correctif Coons. |
| [**D2D1InvertMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1invertmatrix) | Tente d’inverser la matrice spécifiée. |
| [**D2D1IsMatrixInvertible**](/windows/desktop/api/d2d1/nf-d2d1-d2d1ismatrixinvertible) | Indique si la matrice spécifiée est réversible. |
| [**D2D1MakeRotateMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makerotatematrix) | Crée une transformation de rotation qui pivote selon l’angle spécifié à propos du point spécifié. |
| [**D2D1MakeSkewMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makeskewmatrix) | Crée une transformation d’inclinaison qui a l’angle de l’axe x, l’angle de l’axe y et le point central spécifiés.  |
| [**\*, opérateur (const D2D1\MATRIX\3X2\F&, const D2D1\MATRIX\3X2\F&)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-setproduct) | Multiplie deux matrices et retourne le résultat. |
| [**BlobGetter**](blobgetter.md) | Appelle un rappel d’accesseur Get de propriété de fonction membre pour une propriété de type BLOB. |
| [**BlobSetter**](blobsetter.md) | Appelle un rappel d’accesseur Set de propriété de fonction membre pour une propriété de type BLOB. |
| [**DeducingBlobGetter**](deducingblobgetter.md) | Déduire la classe et les arguments, puis appelle un rappel d’accesseur Get de propriété de fonction membre pour une propriété de type BLOB. |
| [**DeducingBlobSetter**](deducingblobsetter.md) | Déduire la classe et les arguments, puis appelle un rappel d’accesseur Set de propriété de fonction membre pour une propriété de type BLOB. |
| [**DeducingStringGetter**](deducingstringgetter.md) | Déduire la classe et les arguments, puis appelle un rappel d’accesseur Get de propriété de fonction membre pour une propriété de type chaîne. |
| [**DeducingStringSetter**](deducingstringsetter.md) | Déduire la classe et les arguments, puis appelle un rappel d’accesseur Set de propriété de fonction membre pour une propriété de type chaîne. |
| [**DeducingValueGetter**](deducingvaluegetter.md) | Déduire la classe et les arguments, puis appelle un rappel d’accesseur Get de propriété de fonction membre pour une propriété de type valeur. |
| [**DeducingValueSetter**](deducingvaluesetter.md) | Déduire la classe et les arguments, puis appelle un rappel d’accesseur Set de propriété de fonction membre pour une propriété de type valeur. |
| [**GetType**](/previous-versions/windows/desktop/legacy/hh847962(v=vs.85)) | Récupère le type de la propriété donnée. |
| [**StringGetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringgetter) | Appelle un rappel d’accesseur Get de propriété de fonction membre pour une propriété de type chaîne. |
| [**StringSetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringsetter) | Appelle un rappel d’accesseur Set de propriété de fonction membre pour une propriété de type chaîne. |
| [**ValueGetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuegetter) | Appelle un rappel d’accesseur Set de propriété de fonction membre pour une propriété de type valeur. |
| [**ValueSetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuesetter) | Appelle un rappel d’accesseur Set de propriété de fonction membre pour une propriété de type valeur. |
| [**D2D1ConvertColorSpace**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1convertcolorspace) | Convertit la couleur donnée d’un colorspace en un autre. |
| [**D2D1SinCos**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1sincos) | Retourne le sinus et le cosinus d’un angle. |
| [**D2D1Tan**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1tan) | Retourne la tangente d'un angle. |
| [**D2D1Vec3Length**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1vec3length) | Retourne la longueur d’un vecteur à trois dimensions. |
| [**PD2D1\PROPERTY\GET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_get_function) | Obtient une propriété à partir d’un effet. |
| [**PD2D1\PROPERTY\SET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_set_function) | Définit une propriété sur un effet. |