---
description: L’interface ICertView est utilisée par les clients autorisés correctement pour afficher la base de données des services de certificats.
ms.assetid: c8f316dd-186b-4e4a-b0ce-561a23b266cb
title: Affichage de la base de données des services de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e63619273ac62eb929bfbdecb23c262f59604f17966792fb5edb84c7efe9e3e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896152"
---
# <a name="viewing-the-certificate-services-database"></a>Affichage de la base de données des services de certificats

L’interface [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) est utilisée par les clients autorisés correctement pour afficher la base de données des services de certificats. Il convient de noter que, dans le cadre du produit expédié, le composant logiciel enfichable MMC de l’autorité de certification peut être utilisé pour afficher la base de données des services de certificats. [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) est fourni pour l’affichage de la base de données par programmation. la prise en charge de l’interface **ICertView** commence par Windows XP.

Un client correctement autorisé signifie un utilisateur qui a reçu l’autorisation d’afficher la base de données des services de certificats. le composant logiciel enfichable MMC de l’autorité de certification peut être utilisé pour accorder ou limiter l’accès à l’affichage de la base de données (sous **Propriétés** de l' [*autorité de certification*](../secgloss/c-gly.md), cliquez sur l’onglet **sécurité** ). En outre, pour utiliser l’objet [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) , la station de travail cliente doit avoir installé les composants du client des services de certificats.

Bien qu’il existe différents scénarios pour l’utilisation de [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) et de ses interfaces associées, l’exemple suivant illustre une séquence possible pour le développement d’une application cliente basée sur **ICertView**:

**Pour afficher la base de données des services de certificats**

1.  Après avoir obtenu une instance de l’objet [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) , appelez [**ICertView :: OpenConnection**](/windows/desktop/api/Certview/nf-certview-icertview-openconnection) pour communiquer avec une [*autorité de certification*](../secgloss/c-gly.md) sur un ordinateur spécifique.
2.  Appelez [**ICertView :: SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) pour spécifier le nombre de colonnes dans la vue ; Cet appel est également utilisé pour spécifier une vue par défaut. Si une vue par défaut n’est pas spécifiée dans l’appel, l’appelant doit appeler [**ICertView :: SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn) pour chacune des colonnes à contenu dans la vue.
3.  Facultatif. Spécifiez des critères de tri et/ou des critères de qualification pour la requête de base de données en appelant la fonction [**ICertView :: SetRestriction**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) . Les critères d’inclusion consistent à informer la vue de récupérer des données en fonction de qualificateurs tels que supérieur à, inférieur à, égal à, etc.
4.  Appelez [**ICertView :: OpenView**](/windows/desktop/api/Certview/nf-certview-icertview-openview) pour récupérer les données dans la vue ; les données de la vue se composent des colonnes demandées au moyen de [**ICertView :: SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) (et si aucune vue par défaut n’a été spécifiée, [**ICertView :: SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn)). Si [**ICertView :: SetRestriction**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) a été appelé, les données des colonnes sont triées et/ou qualifiées. **ICertView :: OpenView** crée un objet [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) , qui peut être utilisé pour énumérer les lignes de la vue.
5.  Utilisez les [](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) méthodes IEnumCERTVIEWROW [**IEnumCERTVIEWROW :: EnumCertViewAttribute**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewattribute), [**IEnumCERTVIEWROW :: EnumCertViewColumn**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewcolumn)et [**IEnumCERTVIEWROW :: EnumCertViewExtension**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewextension) pour récupérer les données d’attribut, de colonne et d’extension comme vous le souhaitez.

 

 
