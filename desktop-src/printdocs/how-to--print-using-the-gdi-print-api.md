---
description: cette rubrique explique comment imprimer à partir d’un programme de Windows natif à l’aide de GDI&\# 160 ; Imprimer&\# 160 ; MobileVBActiveX.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: 'Comment : imprimer à l’aide de l’API d’impression GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19832ef93a80cc537d16136ac751cb20fd8664d7d1d31d295568de68d6dd846
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091929"
---
# <a name="how-to-print-using-the-gdi-print-api"></a>Comment : imprimer à l’aide de l’API d’impression GDI

cette rubrique explique comment imprimer à partir d’un programme de Windows natif à l’aide de l' [API d’impression GDI](gdi-printing.md).

## <a name="overview"></a>Vue d’ensemble

l’impression fait généralement partie intégrante d’un programme de Windows natif. il ne s’agit donc pas d’une fonctionnalité que vous pouvez ajouter facilement après avoir écrit le programme. lors de la conception d’un programme pour Windows 7, vous devez envisager d’utiliser l' [API d’impression XPS](xps-printing.md) pour fournir la fonctionnalité d’impression, car elle offre la plus grande compatibilité à l’avenir. les programmes qui doivent s’exécuter sur Windows Vista et les versions antérieures de Windows utiliseront très probablement l' [API d’impression GDI](gdi-printing.md) pour fournir des fonctionnalités d’impression. l’api d’impression GDI est également prise en charge dans Windows 7, mais elle est plus limitée que l’api d’impression XPS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’impression](using-printing.md)
</dt> <dt>

[comment imprimer à partir d’une application Windows](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



