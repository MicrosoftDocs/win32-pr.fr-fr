---
title: Format BC6H
description: Le format BC6H est un format de compression de texture conçu pour prendre en charge les espaces de couleurs HDR (large-Dynamic Range) dans les données sources.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27422e177e98ecdc53b4152ba0514866f5ad75216e9ef789145d1af882a645d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633819"
---
# <a name="bc6h-format"></a>Format BC6H

Le format BC6H est un format de compression de texture conçu pour prendre en charge les espaces de couleurs HDR (large-Dynamic Range) dans les données sources.

-   [À propos du format BC6H/DXGI \_ \_ BC6H](/windows)
-   [Implémentation de BC6H](#bc6h-implementation)
-   [Décodage du format BC6H](#decoding-the-bc6h-format)
-   [Format de point de terminaison compressé BC6H](#bc6h-compressed-endpoint-format)
-   [Extension de signe pour les valeurs de point de terminaison](#sign-extension-for-endpoint-values)
-   [Transformer inversion pour les valeurs de point de terminaison](#transform-inversion-for-endpoint-values)
-   [DÉQUANTIFICATION des points de terminaison de couleur](#unquantization-of-color-endpoints)
-   [Rubriques connexes](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a>À propos du format BC6H/DXGI \_ \_ BC6H

Le format BC6H fournit une compression de haute qualité pour les images qui utilisent trois canaux de couleur HDR, avec une valeur de 16 bits pour chaque canal de couleur de la valeur (16:16:16). Il n’existe pas de prise en charge d’un canal alpha.

BC6H est spécifié par les valeurs d' \_ énumération de format dxgi suivantes :

-   **Dxgi \_ FORMAT \_ BC6H non \_ typé**.
-   **Dxgi \_ FORMAT \_ BC6H \_ UF16**. Ce format BC6H n’utilise pas de bit de signe dans les valeurs de canaux de couleurs à virgule flottante 16 bits.
-   **Dxgi \_ FORMAT \_ BC6H \_ SF16**. Ce format BC6H utilise un bit de signe dans les valeurs de canaux de couleurs à virgule flottante 16 bits.

> [!Note]  
> Le format à virgule flottante de 16 bits pour les canaux de couleur est souvent appelé format à virgule flottante « demi-point ». Ce format utilise la disposition en bits suivante :
>
> |  Format                     | Disposition des bits                                                |
> |-----------------------|-------------------------------------------------|
> | UF16 (unsigned float) | 5 bits d’exposant + 11 bits de mantisse              |
> | SF16 (float signé)   | 1 bit de signe + 5 bits d’exposant + 10 bits de mantisse |
>
> 
>
>  

 

Le format BC6H peut être utilisé pour les ressources de texture [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (y compris les tableaux), Texture3D ou TextureCube (y compris les tableaux). De même, ce format s’applique à toutes les surfaces de la carte MIP associées à ces ressources.

BC6H utilise une taille de bloc fixe de 16 octets (128 bits) et une taille de vignette fixe de texels 4x4. Comme avec les formats BC précédents, les images de texture plus volumineuses que la taille de vignette prise en charge (4x4) sont compressées à l’aide de plusieurs blocs. Cette identité d’adressage s’applique également aux images à trois dimensions, MIP-Maps, cubemaps et les tableaux de texture. Toutes les vignettes d’image doivent avoir le même format.

Voici quelques remarques importantes concernant le format BC6H :

-   BC6H prend en charge la dénormalisation à virgule flottante, mais ne prend pas en charge INF (Infinity) et NaN (not a Number). L’exception est le mode signé de BC6H (DXGI \_ format \_ BC6H \_ SF16), qui prend en charge-INF (infini négatif). Notez que cette prise en charge pour-INF est simplement un artefact du format lui-même et n’est pas spécifiquement pris en charge par les encodeurs pour ce format. En général, lorsque des encodeurs rencontrent des données d’entrée INF (positives ou négatives) ou NaN, ils doivent \\ convertir ces données en valeur de représentation non-INF autorisée maximale et mapper Nan à 0 avant la compression.
-   BC6H ne prend pas en charge un canal alpha.
-   Le décodeur BC6H effectue la décompression avant d’effectuer un filtrage de texture.
-   La décompression BC6H doit être de bits correcte ; autrement dit, le matériel doit retourner des résultats qui sont identiques au décodeur décrit dans cette documentation.

## <a name="bc6h-implementation"></a>Implémentation de BC6H

Un bloc BC6H comprend des bits de mode, des points de terminaison compressés, des index compressés et un index de partition facultatif. Ce format spécifie 14 modes différents.

Une couleur de point de terminaison est stockée sous la forme d’un triplet RVB. BC6H définit une palette de couleurs sur une ligne approximative sur un certain nombre de points de terminaison de couleur définis. En outre, selon le mode, une vignette peut être divisée en deux régions ou traitée comme une seule région, où une vignette à deux régions a un ensemble distinct de points de terminaison de couleur pour chaque région. BC6H stocke un index de palette par Texel.

Dans le cas de deux régions, il existe 32 partitions possibles.

## <a name="decoding-the-bc6h-format"></a>Décodage du format BC6H

Le pseudo-code ci-dessous montre les étapes à suivre pour décompresser le pixel à (x, y) en fonction du bloc BC6H de 16 octets.

``` syntax
decompress_bc6h(x, y, block)
{
    mode = extract_mode(block);
    endpoints;
    index;
    
    if(mode.type == ONE)
    {
        endpoints = extract_compressed_endpoints(mode, block);
        index = extract_index_ONE(x, y, block);
    }
    else //mode.type == TWO
    {
        partition = extract_partition(block);
        region = get_region(partition, x, y);
        endpoints = extract_compressed_endpoints(mode, region, block);
        index = extract_index_TWO(x, y, partition, block);
    }
    
    unquantize(endpoints);
    color = interpolate(index, endpoints);
    finish_unquantize(color);
}
```

Le tableau suivant contient le nombre de bits et les valeurs pour chacun des 14 formats possibles pour les blocs BC6H. 

| Mode | Index de partition | Partition | Points de terminaison de couleur                  | Bits de mode      |
|------|-------------------|-----------|----------------------------------|----------------|
| 1    | 46 bits           | 5 bits    | 75 bits (10,555, 10,555, 10,555) | 2 bits (00)    |
| 2    | 46 bits           | 5 bits    | 75 bits (7666, 7666, 7666)       | 2 bits (01)    |
| 3    | 46 bits           | 5 bits    | 72 bits (11,555, 11,444, 11,444) | 5 bits (00010) |
| 4    | 46 bits           | 5 bits    | 72 bits (11,444, 11,555, 11,444) | 5 bits (00110) |
| 5    | 46 bits           | 5 bits    | 72 bits (11,444, 11,444, 11,555) | 5 bits (01010) |
| 6    | 46 bits           | 5 bits    | 72 bits (9555, 9555, 9555)       | 5 bits (01110) |
| 7    | 46 bits           | 5 bits    | 72 bits (8666, 8555, 8555)       | 5 bits (10010) |
| 8    | 46 bits           | 5 bits    | 72 bits (8555, 8666, 8555)       | 5 bits (10110) |
| 9    | 46 bits           | 5 bits    | 72 bits (8555, 8555, 8666)       | 5 bits (11010) |
| 10   | 46 bits           | 5 bits    | 72 bits (6666, 6666, 6666)       | 5 bits (11110) |
| 11   | 63 bits           | 0 bits    | 60 bits (10,10, 10,10, 10,10)    | 5 bits (00011) |
| 12   | 63 bits           | 0 bits    | 60 bits (11,9, 11,9, 11,9)       | 5 bits (00111) |
| 13   | 63 bits           | 0 bits    | 60 bits (12,8, 12,8, 12,8)       | 5 bits (01011) |
| 14   | 63 bits           | 0 bits    | 60 bits (16,4, 16,4, 16,4)       | 5 bits (01111) |



 

Chaque format de cette table peut être identifié de manière unique par les bits de mode. Les dix premiers modes sont utilisés pour les vignettes de deux régions, et le champ de bits de mode peut avoir deux ou cinq bits de long. Ces blocs comportent également des champs pour les points de terminaison de couleur compressés (72 ou 75 bits), la partition (5 bits) et les index de partition (46 bits).

Pour les points de terminaison de couleur compressés, les valeurs du tableau précédent indiquent la précision des points de terminaison RVB stockés et le nombre de bits utilisés pour chaque valeur de couleur. Par exemple, le mode 3 spécifie un niveau de précision de point de terminaison de couleur 11 et le nombre de bits utilisés pour stocker les valeurs Delta des points de terminaison transformés pour les couleurs rouge, bleu et vert (respectivement, 5, 4 et 4). Le mode 10 n’utilise pas la compression Delta et stocke à la place les quatre points de terminaison de couleur de manière explicite.

Les quatre derniers modes de blocage sont utilisés pour les vignettes d’une région, où le champ de mode est de 5 bits. Ces blocs ont des champs pour les points de terminaison (60 bits) et les index compressés (63 bits). Le mode 11 (comme le mode 10) n’utilise pas la compression Delta et stocke à la place les deux points de terminaison de couleur de manière explicite.

Les modes 10011, 10111, 11011 et 11111 (non affichés) sont réservés. N’utilisez pas celles-ci dans votre encodeur. Si le matériel reçoit des blocs avec l’un de ces modes spécifiés, le bloc décompressé résultant doit contenir uniquement des zéros dans tous les canaux, sauf pour le canal alpha.

Pour BC6H, le canal alpha doit toujours retourner 1,0 quel que soit le mode.

### <a name="bc6h-partition-set"></a>Ensemble de partitions BC6H

Il existe 32 jeux de partitions possibles pour une vignette de deux régions, qui sont définis dans le tableau ci-dessous. Chaque bloc 4x4 représente une forme unique.

![Table des jeux de partitions bc6h](images/bc6h-partition-sets.png)

Dans ce tableau de jeux de partitions, l’entrée en gras et soulignée est l’emplacement de l’index de correction pour le sous-ensemble 1 (qui est spécifié avec un bit moins). L’index de correction pour le sous-ensemble 0 est toujours l’index 0, car le partitionnement est toujours organisé de telle sorte que l’index 0 soit toujours dans le sous-ensemble 0. L’ordre des partitions va de l’angle supérieur gauche à l’angle inférieur droit, en les déplaçant de gauche à droite, puis de haut en bas.

## <a name="bc6h-compressed-endpoint-format"></a>Format de point de terminaison compressé BC6H

![champs de bits pour les formats de point de terminaison compressés bc6h](images/bc6h-headers-med.png)

Ce tableau montre les champs de bits des points de terminaison compressés en tant que fonction du format de point de terminaison, chaque colonne spécifiant un encodage et chaque ligne spécifiant un champ de bits. Cette approche utilise 82 bits pour les vignettes à deux régions et 65 bits pour les vignettes d’une région. Par exemple, les 5 premiers bits pour l’encodage d’une région \[ 16 4 \] ci-dessus (plus précisément la colonne la plus à droite) sont bits m \[ 4:0 \] , les 10 bits suivants sont bits RW \[ 9:0 \] , et ainsi de suite avec les 6 derniers bits contenant BW \[ 10:15 \] .

Les noms de champs dans le tableau ci-dessus sont définis comme suit :

| Champ | Variable          |
|-------|-------------------|
| m     | mode              |
| d     | index de forme       |
| grave    | Endpt \[ 0 \] . \[0\] |
| RX    | Endpt \[ 0 \] . B \[ 0\] |
| quêtes    | Endpt \[ 1 \] . \[0\] |
| cm    | Endpt \[ 1 \] . B \[ 0\] |
| entrepôt    | Endpt \[ 0 \] . \[1\] |
| GX    | Endpt \[ 0 \] . B \[ 1\] |
| GY    | Endpt \[ 1 \] . \[1\] |
| gz    | Endpt \[ 1 \] . B \[ 1\] |
| p.c.    | Endpt \[ 0 \] . A \[ 2\] |
| BX    | Endpt \[ 0 \] . B \[ 2\] |
| by    | Endpt \[ 1 \] . A \[ 2\] |
| Via    | Endpt \[ 1 \] . B \[ 2\] |



 

Endpt \[ i \] , où i est égal à 0 ou 1, fait référence respectivement au 0 ou au 1er ensemble de points de terminaison.

## <a name="sign-extension-for-endpoint-values"></a>Extension de signe pour les valeurs de point de terminaison

Pour les vignettes de deux régions, quatre valeurs de point de terminaison peuvent être étendues. Endpt \[ 0 \] . Un est signé uniquement si le format est un format signé ; les autres points de terminaison sont signés uniquement si le point de terminaison a été transformé ou si le format est un format signé. Le code ci-dessous illustre l’algorithme permettant d’étendre le signe des valeurs de point de terminaison à deux régions.

``` syntax
static void sign_extend_two_region(Pattern &p, IntEndpts endpts[NREGIONS_TWO])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
      if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
      if (p.transformed || BC6H::FORMAT == SIGNED_F16)
      {
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
        endpts[1].A[i] = SIGN_EXTEND(endpts[1].A[i], p.chan[i].delta[1]);
        endpts[1].B[i] = SIGN_EXTEND(endpts[1].B[i], p.chan[i].delta[2]);
      }
    }
}
```

Pour les vignettes d’une région, le comportement est le même, uniquement avec Endpt \[ 1 \] supprimé.

``` syntax
static void sign_extend_one_region(Pattern &p, IntEndpts endpts[NREGIONS_ONE])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
    if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
    if (p.transformed || BC6H::FORMAT == SIGNED_F16) 
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
    }
}
```

## <a name="transform-inversion-for-endpoint-values"></a>Transformer inversion pour les valeurs de point de terminaison

Pour les vignettes de deux régions, la transformation applique l’inverse de l’encodage de différence, en ajoutant la valeur de base à Endpt \[ 0 \] . À trois autres entrées pour un total de 9 opérations d’ajout. Dans l’image ci-dessous, la valeur de base est représentée sous la forme « a0 » et a la précision à virgule flottante la plus élevée. « A1 », « B0 » et « B1 » sont tous des deltas calculés à partir de la valeur d’ancrage, et ces valeurs Delta sont représentées par une précision inférieure. (A0 correspond à Endpt \[ 0 \] . A, B0 correspond à Endpt \[ 0 \] . B, a1 correspond à Endpt \[ 1 \] . A, et B1 correspond à Endpt \[ 1 \] . B.)

![calcul des valeurs de point de terminaison d’inversion de transformation](images/bc6h-transform-inverse.png)

Pour les vignettes d’une région, il n’y a qu’un seul décalage Delta, et donc seulement 3 opérations d’ajout.

Le décompresseur doit s’assurer que les résultats de la transformation inverse ne dépassent pas la précision de Endpt \[ 0 \] . a. Dans le cas d’un dépassement de capacité, les valeurs résultant de la transformation inverse doivent être encapsulées dans le même nombre de bits. Si la précision de a0 est de « p » bits, l’algorithme de transformation est le suivant :

`B0 = (B0 + A0) & ((1 << p) - 1)`

Pour les formats signés, les résultats du calcul Delta doivent également être étendus. Si l’opération d’extension de signe prend en compte l’extension des deux signes, où 0 est positif et 1 est négatif, l’extension de signe 0 s’occupe de la bride ci-dessus. De même, après la bride ci-dessus, seule une valeur de 1 (négatif) doit être une extension de signe.

## <a name="unquantization-of-color-endpoints"></a>DÉQUANTIFICATION des points de terminaison de couleur

Étant donné les points de terminaison non compressés, l’étape suivante consiste à effectuer une DÉQUANTIFICATION initiale des points de terminaison de couleur. Cela implique trois étapes :

-   Une non-quantification des palettes de couleurs
-   Interpolation des palettes
-   Finalisation de la DÉQUANTIFICATION

En séparant le processus de DÉQUANTIFICATION en deux parties (la DÉQUANTIFICATION de la palette de couleurs avant l’interpolation et la DÉQUANTIFICATION finale après l’interpolation) réduit le nombre d’opérations de multiplication requises par rapport à un processus de DÉQUANTIFICATION complet avant l’interpolation de palette.

Le code ci-dessous illustre le processus de récupération des estimations des valeurs de couleur 16 bits d’origine, puis l’utilisation des valeurs de pondération fournies pour ajouter 6 valeurs de couleur supplémentaires à la palette. La même opération est effectuée sur chaque canal.

``` syntax
int aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
int aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

// c1, c2: endpoints of a component
void generate_palette_unquantized(UINT8 uNumIndices, int c1, int c2, int prec, UINT16 palette[NINDICES])
{
    int* aWeights;
    if(uNumIndices == 8)
        aWeights = aWeight3;
    else  // uNumIndices == 16
        aWeights = aWeight4;

    int a = unquantize(c1, prec); 
    int b = unquantize(c2, prec);

    // interpolate
    for(int i = 0; i < uNumIndices; ++i)
        palette[i] = finish_unquantize((a * (64 - aWeights[i]) + b * aWeights[i] + 32) >> 6);
}
```

L’exemple de code suivant illustre le processus d’interpolation, avec les observations suivantes :

-   Étant donné que la plage complète des valeurs de couleur pour la fonction **unquantification** (ci-dessous) est comprise entre-32768 et 65535, l’interpolateur est implémenté à l’aide de l’arithmétique signée 17 bits.
-   Après l’interpolation, les valeurs sont passées à la fonction de non **\_ quantification** (décrite dans le troisième exemple de cette section), qui applique la mise à l’échelle finale.
-   Tous les décompresseurs de matériel sont requis pour retourner des résultats de bits précis avec ces fonctions.

``` syntax
int unquantize(int comp, int uBitsPerComp)
{
    int unq, s = 0;
    switch(BC6H::FORMAT)
    {
    case UNSIGNED_F16:
        if(uBitsPerComp >= 15)
            unq = comp;
        else if(comp == 0)
            unq = 0;
        else if(comp == ((1 << uBitsPerComp) - 1))
            unq = 0xFFFF;
        else
            unq = ((comp << 16) + 0x8000) >> uBitsPerComp;
        break;

    case SIGNED_F16:
        if(uBitsPerComp >= 16)
            unq = comp;
        else
        {
            if(comp < 0)
            {
                s = 1;
                comp = -comp;
            }

            if(comp == 0)
                unq = 0;
            else if(comp >= ((1 << (uBitsPerComp - 1)) - 1))
                unq = 0x7FFF;
            else
                unq = ((comp << 15) + 0x4000) >> (uBitsPerComp-1);

            if(s)
                unq = -unq;
        }
        break;
    }
    return unq;
}
```

**terminer la \_ désquantification** est appelé après l’interpolation de palette. La fonction **unquantificateur** reporte la mise à l’échelle de 31/32 pour Signed, 31/64 pour unsigned. Ce comportement est nécessaire pour récupérer la valeur finale dans une demi-plage valide (-0x7BFF ~ 0x7BFF) une fois l’interpolation de palette terminée afin de réduire le nombre de multiplications nécessaires. **Terminer \_ unquantificateur** applique la mise à l’échelle finale et retourne une valeur **short non signée** qui est réinterprétée en **deux**.

``` syntax
unsigned short finish_unquantize(int comp)
{
    if(BC6H::FORMAT == UNSIGNED_F16)
    {
        comp = (comp * 31) >> 6;                                         // scale the magnitude by 31/64
        return (unsigned short) comp;
    }
    else // (BC6H::FORMAT == SIGNED_F16)
    {
        comp = (comp < 0) ? -(((-comp) * 31) >> 5) : (comp * 31) >> 5;   // scale the magnitude by 31/32
        int s = 0;
        if(comp < 0)
        {
            s = 0x8000;
            comp = -comp;
        }
        return (unsigned short) (s | comp);
    }
}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Compression de bloc de texture dans Direct3D 11](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 