---
title: Entrées Phone-Book
description: Téléphone-entrées de livre contiennent les informations nécessaires pour établir une connexion RAS. Un utilisateur ou un administrateur peut utiliser la boîte de dialogue accès réseau à distance pour créer, modifier et numéroter les entrées de l’annuaire téléphonique.
ms.assetid: 971d7020-f9fd-42d1-97c3-79ad6eba6964
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea62595504229dd5dd920385a92214156a7d112774cb3fefbaff3f1b5edc7cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789819"
---
# <a name="phone-book-entries"></a>Entrées Phone-Book

Téléphone-entrées de livre contiennent les informations nécessaires pour établir une connexion RAS. Un utilisateur ou un administrateur peut utiliser la boîte de dialogue **accès réseau à distance** pour créer, modifier et numéroter les entrées de l’annuaire téléphonique.

à partir de Windows NT Server 4,0, le système prend en charge les fonctions décrites pour Windows 95, ainsi qu’un certain nombre de fonctions supplémentaires qu’une application peut utiliser pour travailler avec des annuaires téléphoniques et des entrées d’annuaire téléphonique.

La fonction [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) affiche une feuille de propriétés qui permet à l’utilisateur de créer, de modifier ou de copier des entrées d’annuaire téléphonique. Les fonctions [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) et [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) appellent la fonction **RasEntryDlg** . Vous pouvez utiliser la fonction [**RasRenameEntry**](/windows/desktop/api/Ras/nf-ras-rasrenameentrya) pour renommer une entrée de l’annuaire téléphonique ou [**RasDeleteEntry**](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya) pour supprimer une entrée. Le [**RasValidateEntryName**](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea) détermine si une chaîne spécifiée a le format correct à utiliser comme nom d’entrée.

Vous pouvez utiliser [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) et [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) pour obtenir et définir des informations supplémentaires sur une entrée d’annuaire téléphonique. Ces fonctions utilisent une structure [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .

Les fonctions [**RasGetCredentials**](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa) et [**RasSetCredentials**](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa) récupèrent et définissent les informations d’identification de l’utilisateur associées à une entrée d’annuaire téléphonique RAS spécifiée. Ces fonctions utilisent une structure [**RASCREDENTIALS**](/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)) .

la fonction [**RasGetCountryInfo**](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa) récupère les informations de numérotation spécifiques au pays ou à la région à partir de la liste de pays Windows téléphonie des pays. **RasGetCountryInfo** utilise la structure [**RASCTRYINFO**](/previous-versions/windows/desktop/legacy/aa376731(v=vs.85)) .

* * Windows 95 : * * prend en charge un ensemble limité de fonctions pour travailler avec des entrées d’annuaire téléphonique. Vous pouvez utiliser les fonctions [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) et [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) pour créer ou modifier une entrée d’annuaire téléphonique. Ces fonctions affichent une boîte de dialogue dans laquelle l’utilisateur peut spécifier des informations sur l’entrée de l’annuaire téléphonique. Vous pouvez utiliser les fonctions [**RasGetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa) et [**RasSetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa) pour définir ou récupérer les paramètres de connexion pour une entrée d’annuaire téléphonique. La fonction [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) récupère un tableau de structures [**RASENTRYNAME**](/previous-versions/windows/desktop/legacy/aa377267(v=vs.85)) qui contiennent les noms d’entrée de l’annuaire téléphonique.

 

 