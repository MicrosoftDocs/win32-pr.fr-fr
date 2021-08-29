---
description: Cette section décrit les structures utilisées avec la \_ fonction d’échappement MXDC et Microsoft XPS Document Converter (MXDC).
ms.assetid: 102dc056-7f65-47d4-8bcd-3b11608bdb9c
title: Structures de code d’échappement MXDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b87ef962be9f8fffa1ae0b2d126cecfda4cc157118f4defd21360b030dc9d30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948389"
---
# <a name="mxdc-escape-code-structures"></a>Structures de code d’échappement MXDC

Cette section décrit les structures utilisées avec la fonction d' [**\_ échappement MXDC**](mxdc-escape.md) et Microsoft XPS Document Converter (MXDC).

## <a name="in-this-section"></a>Dans cette section



| Structure                                                                              | Description                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MXDC \_ \_ en-tête d’échappement \_ T**](mxdcescapeheader.md)<br/>                         | La structure T de l' [**\_ \_ \_ en-tête d’échappement MXDC**](/windows/desktop/printdocs/mxdcescapeheader) contient le code d’opération d’un appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec [**MXDC \_ Escape**](mxdc-escape.md) comme paramètre *nEscape* . Il fournit également la taille des mémoires tampons d’entrée et de sortie.<br/>  |
| [**MXDC d' \_ extraire les données de nom de \_ fichier \_ \_ T**](mxdcgetfilenamedata.md)<br/>                 | La structure [**MXDC \_ obtenir des \_ \_ données de \_ nom**](/windows/desktop/printdocs/mxdcgetfilenamedata) de fichier contient le chemin d’accès complet et le nom de fichier d’un fichier de sortie Microsoft XPS Document Converter (MXDC).<br/>                                                                                                     |
| [**MXDC \_ PRINTTICKET \_ Escape \_ T**](mxdcprintticketescape.md)<br/>               | La structure [**MXDC \_ PrintTicket \_ Escape \_ t**](mxdcprintticketescape.md) est une structure d' [**\_ \_ en-tête d’échappement MXDC \_**](mxdcescapeheader.md) concaténée avec une structure de [**\_ \_ données \_ MXDC PrintTicket**](mxdcprintticketpassthrough.md) .<br/>                            |
| [**\_données MXDC \_ PRINTTICKET \_ T**](mxdcprintticketpassthrough.md)<br/>            | La structure [**MXDC \_ PRINTTICKET \_ Data \_ T**](/windows/desktop/printdocs/mxdcprintticketpassthrough) contient un ticket d’impression de document XPS, qui contient les paramètres d’imprimante et de travail d’impression, à transmettre au fichier de sortie Microsoft XPS Document Converter (MXDC) sans aucun traitement.<br/>              |
| [**MXDC \_ S0PAGE \_ données \_ T**](mxdcs0pagedata.md)<br/>                             | La structure [**MXDC \_ S0PAGE \_ Data \_ T**](/windows/desktop/printdocs/mxdcs0pagedata) contient une page de document XPS à transmettre au fichier de sortie Microsoft XPS Document Converter (MXDC) sans aucun traitement.<br/>                                                                                  |
| [**MXDC \_ S0PAGE \_ passthrough \_ Escape \_ T**](mxdcs0pagepassthroughescape.md)<br/> | La structure [**MXDC \_ S0PAGE \_ passthrough \_ Escape \_ t**](/windows/desktop/printdocs/mxdcs0pagepassthroughescape) est une structure d' [**\_ \_ en-tête d’échappement MXDC \_**](mxdcescapeheader.md) concaténée avec une structure [**MXDC \_ S0PAGE \_ Data \_ T**](mxdcs0pagedata.md) .<br/>                             |
| [**MXDC \_ S0PAGE \_ Resource \_ Escape \_ T**](mxdcs0pageresourceescape.md)<br/>       | La structure d’échappement de la [**\_ ressource MXDC S0PAGE \_ \_ \_**](/windows/desktop/printdocs/mxdcs0pageresourceescape) est une structure d' [**\_ \_ en-tête d’échappement \_ MXDC**](mxdcescapeheader.md) concaténée avec une structure de [**\_ \_ \_ ressource \_ t MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) .<br/>                   |
| [**\_Ressource MXDC \_ XPS \_ S0PAGE \_ T**](mxdcxpss0pageresource.md)<br/>             | La structure de la [**\_ ressource MXDC XPS \_ S0PAGE \_ \_**](/windows/desktop/printdocs/mxdcxpss0pageresource) contient des informations sur une ressource, telle qu’une image ou une police, qui est associée à une page de document XPS et doit être transmise au fichier de sortie Microsoft XPS Document Converter (MXDC).<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**MXDC \_ échappement**](mxdc-escape.md)
</dt> </dl>

 

