---
title: L’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’applications du Windows Store n’est pas pris en charge
description: L’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’applications du Windows Store n’est pas pris en charge
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0846b56b1d6c2367c46e4adf82dac011c49fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727693"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>L’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’applications du Windows Store n’est pas pris en charge

## <a name="platforms"></a>Plateformes

<dl> Clients-Windows 8,1  
Serveurs-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

L’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’une application du Windows Store n’est pas pris en charge et peut entraîner des résultats inattendus.

## <a name="manifestations"></a>Manifestations

Au démarrage de l’application, le mode IME est défini sur les valeurs par défaut suivantes :



|          | Panneau de saisie du logiciel | Clavier matériel |
|----------|----------------------|-------------------|
| KOR, JPN | Il en va                   | Désactivé               |
| CHS, CHT | Il en va                   | Il en va                |



 

## <a name="solution"></a>Solution

Les développeurs peuvent contrôler le mode IME par défaut en spécifiant une valeur d’étendue d’entrée pour le champ.

Le mode IME pour une étendue d’entrée spécifiée est déterminé par chaque IME. Les développeurs ne peuvent pas spécifier le mode IME.

## <a name="resources"></a>Ressources

-   [Énumération InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [ImmSetConversionStatus](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))

 

 