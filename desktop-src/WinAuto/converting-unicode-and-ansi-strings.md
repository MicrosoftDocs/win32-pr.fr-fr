---
title: Conversion de chaînes Unicode et ANSI
description: Microsoft Active Accessibility utilise des chaînes Unicode telles que définies par le type de données BSTR.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520897"
---
# <a name="converting-unicode-and-ansi-strings"></a>Conversion de chaînes Unicode et ANSI

Microsoft Active Accessibility utilise des chaînes Unicode telles que définies par le type de données **BSTR** . Si votre application n’utilise pas de chaînes Unicode, ou si vous souhaitez convertir des chaînes pour certains appels d’API, utilisez les fonctions de Microsoft Win32 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) et [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) pour effectuer la conversion nécessaire.

Utilisez [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) pour convertir une chaîne Unicode en une chaîne ANSI. La fonction [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) convertit une chaîne ANSI en chaîne Unicode.

Utilisez [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) et [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) pour allouer et libérer des types de données **BSTR** .

pour plus d’informations sur ces fonctions de chaîne, consultez leurs références dans le kit de développement logiciel (SDK) Windows.

 

 