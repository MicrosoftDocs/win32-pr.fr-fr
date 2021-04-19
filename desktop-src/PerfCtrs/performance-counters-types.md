---
description: PDH définit les types de données suivants.
ms.assetid: 8a2e8683-502a-4893-8b4f-5e2cf464a933
title: Types de données des compteurs de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f9800288494eb82f675265b6e0b801c783668d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543702"
---
# <a name="performance-counters-data-types"></a>Types de données des compteurs de performances

## <a name="performance-data-helper-pdh-types"></a>Types d’assistance de données de performances (PDH)

Les consommateurs qui utilisent les fonctions [d’assistance des données de performance (PDH)](using-the-pdh-functions-to-consume-counter-data.md) utilisent les types suivants :

| Type de données | Description
|-----------|------------
| **\_HQUERY PDH**   | Handle d’une requête. La fonction [**PdhOpenQuery**](/windows/win32/api/pdh/nf-pdh-pdhopenqueryw) retourne ce descripteur. Fermez le descripteur à l’aide de [**PdhCloseQuery**](/windows/win32/api/pdh/nf-pdh-pdhclosequery).
| **\_HCOUNTER PDH** | Handle d’un compteur. La fonction [**PdhAddCounter**](/windows/win32/api/pdh/nf-pdh-pdhaddcounterw) retourne ce descripteur. Fermez le handle à l’aide de [**PdhRemoveCounter**](/windows/win32/api/pdh/nf-pdh-pdhremovecounter) ou en fermant le handle de la requête qui contient le compteur. N’appelez pas **PdhRemoveCounter** sur un compteur si la requête correspondante a déjà été fermée. PDH gère la liaison entre les compteurs et les requêtes et ferme automatiquement les descripteurs de compteur lorsque le handle de requête correspondant est fermé.
| **\_HLOG PDH**     | Handle vers un fichier journal. Les fonctions [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) et [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) retournent ce handle. Fermez le descripteur à l’aide de [**PdhCloseLog**](/windows/win32/api/pdh/nf-pdh-pdhcloselog).
| **\_État PDH**   | Valeur d’État PDH. Toutes les fonctions PDH retournent une valeur de type **PDH \_ Status**. Si la fonction réussit, la valeur de retour est une erreur de \_ réussite. Dans le cas contraire, la fonction retourne un [code d’erreur système](/windows/desktop/Debug/system-error-codes) ou un [code d’erreur PDH](pdh-error-codes.md).
