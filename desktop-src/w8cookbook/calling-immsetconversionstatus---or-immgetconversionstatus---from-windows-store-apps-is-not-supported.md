---
title: l’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’applications Windows store n’est pas pris en charge
description: l’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’applications Windows store n’est pas pris en charge
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8ca572b1ea88ca988ecba66231a87cb6ae6db2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234894"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>l’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’applications Windows store n’est pas pris en charge

## <a name="platforms"></a>Plateformes

<dl> Clients-Windows 8,1  
serveurs-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

l’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’une application Windows Store n’est pas pris en charge et peut entraîner des résultats inattendus.

## <a name="manifestations"></a>Manifestations

Au démarrage de l’application, le mode IME est défini sur les valeurs par défaut suivantes :



| &nbsp;   | Panneau de saisie du logiciel | Clavier matériel |
|----------|----------------------|-------------------|
| KOR, JPN | Activé                   | Désactivé               |
| CHS, CHT | Activé                   | Activé                |



 

## <a name="solution"></a>Solution

Les développeurs peuvent contrôler le mode IME par défaut en spécifiant une valeur d’étendue d’entrée pour le champ.

Le mode IME pour une étendue d’entrée spécifiée est déterminé par chaque IME. Les développeurs ne peuvent pas spécifier le mode IME.

## <a name="resources"></a>Ressources

-   [Énumération InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [ImmSetConversionStatus](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))

 

 