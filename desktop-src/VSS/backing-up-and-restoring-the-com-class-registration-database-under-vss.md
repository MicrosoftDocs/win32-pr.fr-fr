---
description: Le modèle COM (Component Object Model) est une norme binaire pour l’écriture de logiciels de composants dans un environnement informatique distribué.
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: Sauvegarde et restauration de la base de données d’inscription de classe COM+ sous VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b248408d3c1a712fa37c55fd851bc7cc72662ac4da91422e6b1086d4b022107
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124579"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a>Sauvegarde et restauration de la base de données d’inscription de classe COM+ sous VSS

Le modèle COM (Component Object Model) est une norme binaire pour l’écriture de logiciels de composants dans un environnement informatique distribué.

Identificateurs de composant (GUID) d’implémentation Win32 d’origine et autre État COM dans le Registre sous **le \_ \_ \\ CLSID racine des classes HKEY**.

La génération actuelle du modèle COM (Component Object Model), COM+, offre une base de données indépendante du Registre pour le stockage des informations d’inscription du composant : la base de données d’inscription de classe COM+.

La base de données d’inscription de classe COM+ prend en charge un enregistreur VSS, qui permet aux demandeurs de sauvegarder la base de données d’inscription à l’aide des données stockées sur un volume copié par cliché instantané.

Pour restaurer la base de données d’inscription COM+, un demandeur doit appeler la méthode [ICOMAdminCatalog :: RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .

Pour plus d’informations sur le writer de base de données d’inscription COM+, consultez la page [enregistreurs VSS](in-box-vss-writers.md).

 

 
