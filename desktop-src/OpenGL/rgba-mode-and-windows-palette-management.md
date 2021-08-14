---
title: Mode rvba et gestion des palettes de Windows
description: Alors que la plupart des applications GDI ont tendance à utiliser l’indexation des couleurs avec des palettes logiques, le mode RVBA est généralement préférable pour les applications OpenGL. Il fonctionne mieux que le mappage des couleurs pour plusieurs effets, tels que l’ombrage, l’éclairage, le brouillard et le mappage de texture.
ms.assetid: 68c35173-e792-4770-9404-5503344f475b
keywords:
- OpenGL sur Windows, mode rvba
- OpenGL sur Windows, gestion de la palette
- Mode RVBA OpenGL
- gestion de la palette OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53016764636cadd9fe85e0478905958788ca2557a308375bc8d6d9826462c6b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932951"
---
# <a name="rgba-mode-and-windows-palette-management"></a>Mode rvba et gestion des palettes de Windows

Alors que la plupart des applications GDI ont tendance à utiliser l’indexation des couleurs avec des palettes logiques, le mode RVBA est généralement préférable pour les applications OpenGL. Il fonctionne mieux que le mappage des couleurs pour plusieurs effets, tels que l’ombrage, l’éclairage, le brouillard et le mappage de texture.

Le mode RVBA utilise des valeurs de couleur rouge, vert et bleu (R, G et B) qui définissent la couleur de chaque pixel de l’affichage. Les valeurs R, G et B spécifient l’intensité de chaque couleur (rouge, vert et bleu); les valeurs sont comprises entre 0,0 (les moins intenses) et 1,0 (les plus intenses). Le nombre de bits pour chaque composant varie selon le matériel utilisé (2, 3, 5, 6 et 8 bits sont possibles). La couleur affichée est le résultat de la somme des trois valeurs de couleur. Si les trois valeurs sont 0,0, le résultat est noir. Si les trois valeurs sont toutes 1,0, le résultat est blanc. D’autres couleurs résultent d’une combinaison de valeurs R, G et B comprises entre 0 et 1,0. Le bit A (alpha) n’est pas utilisé pour spécifier la couleur.

L’affichage Super VGA standard utilise des palettes avec huit bits de couleur par pixel. Les huit bits sont lus à partir de la mémoire tampon et utilisés comme index dans la palette système pour obtenir les valeurs R, G et B. Quand une palette RVB est sélectionnée et réalisée dans un contexte de périphérique, OpenGL peut effectuer un rendu en utilisant le mode RVBA.

Étant donné qu’il y a huit bits de couleur par pixel, OpenGL met l’accent sur l’utilisation d’une palette à trois trois trois-deux. « Trois-trois-deux » fait référence à la façon dont les données de couleur sont gérées par la palette matérielle ou physique. Les couleurs rouge (R) et vert (G) sont spécifiées par trois bits ; le bleu (B) est spécifié par deux bits. Le rouge est le bit le moins significatif et le bleu est le bit le plus significatif.

Vous déterminez les couleurs de la palette logique de votre application avec des structures [PaletteEntry](/previous-versions//dd162769(v=vs.85)) . En général, vous créez un tableau de structures **PaletteEntry** pour spécifier l’ensemble de la table d’entrée de palette de la palette logique.

## <a name="rgba-mode-palette-sample"></a>Exemple de palette en mode RVBA

Le fragment de code suivant montre comment vous pouvez créer une palette à trois trois-deux.


```C++
/* 
 * win8map.c - program to create an 8-bit RGB color map for  
 * use with OpenGL 
 * 
 * For OpenGL RGB rendering you need to know red, green, & blue  
 * component bit sizes and positions. On 8 bit palette devices you need  
 * to create a logical palette that has the correct RGBA values for all  
 * 256 possible entries. This program creates an 8 bit RGBA color cube  
 * with a default gamma of 1.4 
 * 
 * Unfortunately, because the standard 20 colors in the system palette  
 * cannot be changed,if you select this palette into an 8-bit display  
 * DC, you will not realize all of the logical palette. The program  
 * changes some of the entries in the logical palette to match enties in  
 * the system palette using a least-squares calculation to find which  
 * entries to replace 
 * 
 * Note: Three bits for red & green and two bits for blue; red is the  
 * least-significant bit and blue is the most-significant bit 
 */ 
 
#include <stdio.h> 
#include <math.h> 
 
#define DEFAULT_GAMMA 1.4F 
 
#define MAX_PAL_ERROR (3*256*256L) 
 
struct colorentry { 
    unsigned char red; 
    unsigned char green; 
    unsigned char blue; 
}; 
 
struct rampentry { 
    struct colorentry color; 
    long defaultindex; 
    unsigned char flags; 
}; 
 
struct defaultentry { 
    struct colorentry color; 
    long rampindex; 
    unsigned char flags; 
}; 
 
/* values for flags */ 
#define EXACTMATCH      0x01 
#define CHANGED         0x02        /* one of the default entries is close */ 
 
/* 
 * These arrays hold bit arrays with a gamma of 1.0  
 * used to convert n bit values to 8-bit values 
 */ 
  
unsigned char threeto8[8] = { 
    0, 0111>>1, 0222>>1, 0333>>1, 0444>>1, 0555>>1, 0666>>1, 0377 
}; 
 
unsigned char twoto8[4] = { 
    0, 0x55, 0xaa, 0xff 
}; 
 
unsigned char oneto8[2] = { 
    0, 255 
}; 
 
struct defaultentry defaultpal[20] = { 
    { 0,   0,   0 }, 
    { 0x80,0,   0 }, 
    { 0,   0x80,0 }, 
    { 0x80,0x80,0 }, 
    { 0,   0,   0x80 }, 
    { 0x80,0,   0x80 }, 
    { 0,   0x80,0x80 }, 
    { 0xC0,0xC0,0xC0 }, 
 
    { 192, 220, 192 }, 
    { 166, 202, 240 }, 
    { 255, 251, 240 }, 
    { 160, 160, 164 }, 
 
    { 0x80,0x80,0x80 }, 
    { 0xFF,0,   0 }, 
    { 0,   0xFF,0 }, 
    { 0xFF,0xFF,0 }, 
    { 0,   0,   0xFF }, 
    { 0xFF,0,   0xFF }, 
    { 0,   0xFF,0xFF }, 
    { 0xFF,0xFF,0xFF } 
}; 
 
struct rampentry rampmap[256]; 
  
void 
gammacorrect(double gamma) 
{ 
    int i; 
    unsigned char v, nv; 
    double dv; 
 
    for (i=0; i<8; i++) { 
        v = threeto8[i]; 
        dv = (255.0 * pow(v/255.0, 1.0/gamma)) + 0.5; 
    nv = (unsigned char)dv; 
    printf("Gamma correct %d to %d (gamma %.2f)\n", v, nv, gamma); 
        threeto8[i] = nv; 
    } 
    for (i=0; i<4; i++) { 
        v = twoto8[i]; 
        dv = (255.0 * pow(v/255.0, 1.0/gamma)) + 0.5; 
    nv = (unsigned char)dv; 
    printf("Gamma correct %d to %d (gamma %.2f)\n", v, nv, gamma); 
        twoto8[i] = nv; 
    } 
    printf("\n"); 
} 
 
main(int argc, char *argv[]) 
{ 
    long i, j, error, min_error; 
    long error_index, delta; 
    double gamma; 
    struct colorentry *pc; 
  
    if (argc == 2) 
        gamma = atof(argv[1]); 
    else 
        gamma = DEFAULT_GAMMA; 
 
    gammacorrect(gamma); 
       
    /* First create a 256 entry RGB color cube */ 
     
    for (i = 0; i < 256; i++) { 
        /* BGR: 2:3:3 */ 
        rampmap[i].color.red = threeto8[(i&7)]; 
        rampmap[i].color.green = threeto8[((i>>3)&7)]; 
        rampmap[i].color.blue = twoto8[(i>>6)&3]; 
    } 
 
    /* Go through the default palette and find exact matches */ 
    for (i=0; i<20; i++) { 
        for(j=0; j<256; j++) { 
            if ( (defaultpal[i].color.red == rampmap[j].color.red) && 
                 (defaultpal[i].color.green == rampmap[j].color.green) && 
                 (defaultpal[i].color.blue == rampmap[j].color.blue)) { 
 
                rampmap[j].flags = EXACTMATCH; 
                rampmap[j].defaultindex = i; 
                defaultpal[i].rampindex = j; 
                defaultpal[i].flags = EXACTMATCH; 
                break; 
            }  
        } 
    } 
 
    /* Now find close matches */             
    for (i=0; i<20; i++) { 
        if (defaultpal[i].flags == EXACTMATCH) 
            continue;         /* skip entries w/ exact matches */ 
        min_error = MAX_PAL_ERROR; 
         
        /* Loop through RGB ramp and calculate least square error */ 
        /* if an entry has already been used, skip it */ 
        for(j=0; j<256; j++) { 
            if (rampmap[j].flags != 0)      /* Already used */ 
                continue; 
                 
            delta = defaultpal[i].color.red - rampmap[j].color.red; 
            error = (delta * delta); 
            delta = defaultpal[i].color.green - rampmap[j].color.green; 
            error += (delta * delta); 
            delta = defaultpal[i].color.blue - rampmap[j].color.blue; 
            error += (delta * delta); 
            if (error < min_error) {        /* New minimum? */ 
                error_index = j; 
                min_error = error; 
            } 
        } 
        defaultpal[i].rampindex = error_index; 
        rampmap[error_index].flags = CHANGED; 
        rampmap[error_index].defaultindex = i; 
    } 
     
    /* First print out the color cube */  
     
    printf("Standard 8-bit RGB color cube with gamma %.2f:\n", gamma); 
    for (i=0; i<256; i++) { 
        pc = &rampmap[i].color;  
        printf("%3ld: (%3-D, %3-D, %3-D)\n", i, pc->red,  
                pc->green, pc->blue); 
     
    } 
    printf("\n"); 
     
    /* Now print out the default entries that have an exact match */ 
 
    for (i=0; i<20; i++) { 
        if (defaultpal[i].flags == EXACTMATCH) { 
            pc = &defaultpal[i].color;  
            printf("Default entry %2ld exactly matched RGB ramp entry  
                      %3ld", i, defaultpal[i].rampindex); 
            printf(" (%3-D, %3-D, %3-D)\n", pc->red, pc->green, pc->blue); 
        } 
    } 
    printf("\n"); 
     
    /* Now print out the closest entries for rest of  
     * the default entries */ 
     
    for (i=0; i<20; i++) { 
        if (defaultpal[i].flags != EXACTMATCH) { 
            pc = &defaultpal[i].color;  
            printf("Default entry %2ld (%3-D, %3-D, %3-D) is close to ", 
                i, pc->red, pc->green, pc->blue); 
            pc = &rampmap[defaultpal[i].rampindex].color; 
            printf("RGB ramp entry %3ld (%3-D, %3-D, %3-D)\n", 
                defaultpal[i].rampindex, pc->red, pc->green, pc->blue); 
        } 
    } 
    printf("\n"); 
     
    /* Print out code to initialize a logical palette  
     * that will not overflow */ 
 
    printf("Here is code you can use to create a logical palette\n"); 
 
    printf("static struct {\n"); 
    printf("    WORD        palVersion;\n"); 
    printf("    WORD        palNumEntries;\n"); 
    printf("    PALETTEENTRY palPalEntries[256];\n"); 
    printf("} rgb8palette = {\n"); 
    printf("    0x300,\n"); 
    printf("    256,\n"); 
 
    for (i=0; i<256; i++) {  
        if (rampmap[i].flags == 0) 
            pc = &rampmap[i].color; 
        else 
            pc = &defaultpal[rampmap[i].defaultindex].color; 
         
        printf("    %3-D, %3-D, %3-D,   0,    /* %ld", 
                pc->red, pc->green, pc->blue, i);  
        if (rampmap[i].flags == EXACTMATCH) 
            printf(" - Exact match with default %d",  
                       rampmap[i].defaultindex); 
        if (rampmap[i].flags == CHANGED) 
            printf(" - Changed to match default %d",  
                       rampmap[i].defaultindex); 
        printf(" */\n"); 
    } 
 
    printf("};\n"); 
    printf("\n    * * *\n\n"); 
    printf("    hpal = CreatePalette((LOGPALETTE *)&rgb8palette);\n"); 
 
    return 0; 
}
```



 

 