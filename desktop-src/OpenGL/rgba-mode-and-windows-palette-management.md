---
title: Mode RVBA et gestion de la palette Windows
description: Alors que la plupart des applications GDI ont tendance à utiliser l’indexation des couleurs avec des palettes logiques, le mode RVBA est généralement préférable pour les applications OpenGL. Il fonctionne mieux que le mappage des couleurs pour plusieurs effets, tels que l’ombrage, l’éclairage, le brouillard et le mappage de texture.
ms.assetid: 68c35173-e792-4770-9404-5503344f475b
keywords:
- OpenGL sur Windows, mode RVBA
- OpenGL sur Windows, gestion de palette
- Mode RVBA OpenGL
- gestion de la palette OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2e04110d1dfe489a145a8de9bdc7c3d9b726acd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510494"
---
# <a name="rgba-mode-and-windows-palette-management"></a><span data-ttu-id="11712-108">Mode RVBA et gestion de la palette Windows</span><span class="sxs-lookup"><span data-stu-id="11712-108">RGBA Mode and Windows Palette Management</span></span>

<span data-ttu-id="11712-109">Alors que la plupart des applications GDI ont tendance à utiliser l’indexation des couleurs avec des palettes logiques, le mode RVBA est généralement préférable pour les applications OpenGL.</span><span class="sxs-lookup"><span data-stu-id="11712-109">While most GDI applications tend to use color-indexing with logical palettes, the RGBA mode is usually preferable for OpenGL applications.</span></span> <span data-ttu-id="11712-110">Il fonctionne mieux que le mappage des couleurs pour plusieurs effets, tels que l’ombrage, l’éclairage, le brouillard et le mappage de texture.</span><span class="sxs-lookup"><span data-stu-id="11712-110">It works better than color mapping for several effects, such as shading, lighting, fog, and texture mapping.</span></span>

<span data-ttu-id="11712-111">Le mode RVBA utilise des valeurs de couleur rouge, vert et bleu (R, G et B) qui définissent la couleur de chaque pixel de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="11712-111">The RGBA mode uses red, green, and blue (R, G, and B) color values that together specify the color of each pixel in the display.</span></span> <span data-ttu-id="11712-112">Les valeurs R, G et B spécifient l’intensité de chaque couleur (rouge, vert et bleu); les valeurs sont comprises entre 0,0 (les moins intenses) et 1,0 (les plus intenses).</span><span class="sxs-lookup"><span data-stu-id="11712-112">The R, G, and B values specify the intensity of each color (red, green, and blue); the values range from 0.0 (least intense) to 1.0 (most intense).</span></span> <span data-ttu-id="11712-113">Le nombre de bits pour chaque composant varie selon le matériel utilisé (2, 3, 5, 6 et 8 bits sont possibles). La couleur affichée est le résultat de la somme des trois valeurs de couleur.</span><span class="sxs-lookup"><span data-stu-id="11712-113">The number of bits for each component varies depending on the hardware used (2, 3, 5, 6, and 8 bits are possible).The color displayed is a result of the sum of the three color values.</span></span> <span data-ttu-id="11712-114">Si les trois valeurs sont 0,0, le résultat est noir.</span><span class="sxs-lookup"><span data-stu-id="11712-114">If all three values are 0.0, the result is black.</span></span> <span data-ttu-id="11712-115">Si les trois valeurs sont toutes 1,0, le résultat est blanc.</span><span class="sxs-lookup"><span data-stu-id="11712-115">If the three values are all 1.0, the result is white.</span></span> <span data-ttu-id="11712-116">D’autres couleurs résultent d’une combinaison de valeurs R, G et B comprises entre 0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="11712-116">Other colors are a result of a combination of values of R, G, and B that fall between 0 and 1.0.</span></span> <span data-ttu-id="11712-117">Le bit A (alpha) n’est pas utilisé pour spécifier la couleur.</span><span class="sxs-lookup"><span data-stu-id="11712-117">The A (alpha) bit isn't used to specify color.</span></span>

<span data-ttu-id="11712-118">L’affichage Super VGA standard utilise des palettes avec huit bits de couleur par pixel.</span><span class="sxs-lookup"><span data-stu-id="11712-118">The standard super-VGA display uses palettes with eight color-bits per pixel.</span></span> <span data-ttu-id="11712-119">Les huit bits sont lus à partir de la mémoire tampon et utilisés comme index dans la palette système pour obtenir les valeurs R, G et B.</span><span class="sxs-lookup"><span data-stu-id="11712-119">The eight bits are read from the buffer and used as an index in the system palette to get the R, G, and B values.</span></span> <span data-ttu-id="11712-120">Quand une palette RVB est sélectionnée et réalisée dans un contexte de périphérique, OpenGL peut effectuer un rendu en utilisant le mode RVBA.</span><span class="sxs-lookup"><span data-stu-id="11712-120">When an RGB palette is selected and realized in a device context, OpenGL can render using the RGBA mode.</span></span>

<span data-ttu-id="11712-121">Étant donné qu’il y a huit bits de couleur par pixel, OpenGL met l’accent sur l’utilisation d’une palette à trois trois trois-deux.</span><span class="sxs-lookup"><span data-stu-id="11712-121">Because there are eight color-bits per pixel, OpenGL emphasizes the use of a three-three-two RGBA palette.</span></span> <span data-ttu-id="11712-122">« Trois-trois-deux » fait référence à la façon dont les données de couleur sont gérées par la palette matérielle ou physique.</span><span class="sxs-lookup"><span data-stu-id="11712-122">"Three-three-two" refers to how the color-bit data is handled by the hardware or physical palette.</span></span> <span data-ttu-id="11712-123">Les couleurs rouge (R) et vert (G) sont spécifiées par trois bits ; le bleu (B) est spécifié par deux bits.</span><span class="sxs-lookup"><span data-stu-id="11712-123">Red (R) and green (G) are each specified by three bits; blue (B) is specified by two bits.</span></span> <span data-ttu-id="11712-124">Le rouge est le bit le moins significatif et le bleu est le bit le plus significatif.</span><span class="sxs-lookup"><span data-stu-id="11712-124">Red is the least-significant bit and blue is the most-significant bit.</span></span>

<span data-ttu-id="11712-125">Vous déterminez les couleurs de la palette logique de votre application avec des structures [PaletteEntry](/previous-versions//dd162769(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="11712-125">You determine the colors of your application's logical palette with [PALETTEENTRY](/previous-versions//dd162769(v=vs.85)) structures.</span></span> <span data-ttu-id="11712-126">En général, vous créez un tableau de structures **PaletteEntry** pour spécifier l’ensemble de la table d’entrée de palette de la palette logique.</span><span class="sxs-lookup"><span data-stu-id="11712-126">Typically you create an array of **PALETTEENTRY** structures to specify the entire palette entry table of the logical palette.</span></span>

## <a name="rgba-mode-palette-sample"></a><span data-ttu-id="11712-127">Exemple de palette en mode RVBA</span><span class="sxs-lookup"><span data-stu-id="11712-127">RGBA Mode Palette Sample</span></span>

<span data-ttu-id="11712-128">Le fragment de code suivant montre comment vous pouvez créer une palette à trois trois-deux.</span><span class="sxs-lookup"><span data-stu-id="11712-128">The following code fragment shows how you can create a three-three-two RGBA palette.</span></span>


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



 

 