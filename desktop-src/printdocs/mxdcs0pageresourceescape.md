---
description: La \_ \_ structure d’échappement de la ressource MXDC S0PAGE \_ \_ est \_ une \_ structure d’en-tête d’échappement MXDC \_ concaténée avec une \_ \_ structure de ressource t MXDC XPS S0PAGE \_ \_ .
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: Structure MXDC_S0PAGE_RESOURCE_ESCAPE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202808"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a>Structure de l’échappement de la \_ ressource MXDC S0PAGE \_ \_ \_

La structure d’échappement de la **\_ ressource MXDC S0PAGE \_ \_ \_** est une structure d' [**\_ \_ en-tête d’échappement \_ MXDC**](mxdcescapeheader.md) concaténée avec une structure de [**\_ \_ \_ ressource \_ t MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a>Membres

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Une [**structure \_ \_ \_ T d’en-tête d’échappement MXDC**](mxdcescapeheader.md) avec son membre **opcode** défini sur MXDCOP \_ définir \_ S0PAGE \_ ressource.

</dd> <dt>

**xpsS0PageResourcePassthrough**
</dt> <dd>

Structure [**de \_ ressource MXDC XPS \_ S0PAGE \_ \_**](mxdcxpss0pageresource.md) représentant une ressource, telle qu’une police ou un fichier image, sur une page de document XPS.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est transmise dans le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) lorsque cette fonction est appelée avec l’échappement [**MXDC \_**](mxdc-escape.md) Escape et que le membre **opcode** de la structure T de l' [**\_ \_ en-tête \_ d’échappement MXDC**](mxdcescapeheader.md) est **MXDCOP définir la \_ \_ \_ ressource S0PAGE**. Le résultat est une ressource de page à envoyer à MXDC.

Allouez de la mémoire pour l’échappement comme indiqué ci-dessous, définissez les champs en fonction des besoins, puis appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit être compris entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); Toutefois, il peut y avoir plus d’un de ces appels entre les appels à **StartPage** et **EndPage**.

La consommation de la diffusion en continu est plus efficace si vous appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec **MXDCOP \_ défini \_ S0PAGE \_** **opcode** de ressource pour chaque ressource sur la page avant d’appeler **ExtEscape** avec l'**opcode** **MXDCOP \_ Set \_ S0PAGE**.  

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mxdc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[Fonctions d’échappement d’imprimante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ échappement**](mxdc-escape.md)
</dt> </dl>

 

