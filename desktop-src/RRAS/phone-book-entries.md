---
title: Entrées Phone-Book
description: Les entrées de l’annuaire téléphonique contiennent les informations nécessaires pour établir une connexion RAS. Un utilisateur ou un administrateur peut utiliser la boîte de dialogue accès réseau à distance pour créer, modifier et numéroter les entrées de l’annuaire téléphonique.
ms.assetid: 971d7020-f9fd-42d1-97c3-79ad6eba6964
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cc01e66b5877c90b81610a5d8cf151b7cb7bd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102133"
---
# <a name="phone-book-entries"></a>Entrées Phone-Book

Les entrées de l’annuaire téléphonique contiennent les informations nécessaires pour établir une connexion RAS. Un utilisateur ou un administrateur peut utiliser la boîte de dialogue **accès réseau à distance** pour créer, modifier et numéroter les entrées de l’annuaire téléphonique.

À compter de Windows NT Server 4,0, le système prend en charge les fonctions décrites pour Windows 95, ainsi qu’un certain nombre de fonctions supplémentaires qu’une application peut utiliser pour travailler avec des annuaires téléphoniques et des entrées d’annuaire téléphonique.

La fonction [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) affiche une feuille de propriétés qui permet à l’utilisateur de créer, de modifier ou de copier des entrées d’annuaire téléphonique. Les fonctions [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) et [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) appellent la fonction **RasEntryDlg** . Vous pouvez utiliser la fonction [**RasRenameEntry**](/windows/desktop/api/Ras/nf-ras-rasrenameentrya) pour renommer une entrée de l’annuaire téléphonique ou [**RasDeleteEntry**](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya) pour supprimer une entrée. Le [**RasValidateEntryName**](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea) détermine si une chaîne spécifiée a le format correct à utiliser comme nom d’entrée.

Vous pouvez utiliser [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) et [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) pour obtenir et définir des informations supplémentaires sur une entrée d’annuaire téléphonique. Ces fonctions utilisent une structure [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .

Les fonctions [**RasGetCredentials**](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa) et [**RasSetCredentials**](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa) récupèrent et définissent les informations d’identification de l’utilisateur associées à une entrée d’annuaire téléphonique RAS spécifiée. Ces fonctions utilisent une structure [**RASCREDENTIALS**](/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)) .

La fonction [**RasGetCountryInfo**](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa) récupère les informations de numérotation spécifiques à un pays ou une région à partir de la liste des pays de la téléphonie Windows. **RasGetCountryInfo** utilise la structure [**RASCTRYINFO**](/previous-versions/windows/desktop/legacy/aa376731(v=vs.85)) .

**Windows 95 :  ** Prend en charge un ensemble limité de fonctions permettant d’utiliser des entrées d’annuaire téléphonique. Vous pouvez utiliser les fonctions [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) et [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) pour créer ou modifier une entrée d’annuaire téléphonique. Ces fonctions affichent une boîte de dialogue dans laquelle l’utilisateur peut spécifier des informations sur l’entrée de l’annuaire téléphonique. Vous pouvez utiliser les fonctions [**RasGetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa) et [**RasSetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa) pour définir ou récupérer les paramètres de connexion pour une entrée d’annuaire téléphonique. La fonction [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) récupère un tableau de structures [**RASENTRYNAME**](/previous-versions/windows/desktop/legacy/aa377267(v=vs.85)) qui contiennent les noms d’entrée de l’annuaire téléphonique.

 

 