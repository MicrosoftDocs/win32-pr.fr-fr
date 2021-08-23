---
description: L’objet session contrôle le processus d’installation.
ms.assetid: 013959d9-900c-45f7-b742-17b0365d6107
title: objet Session (Windows Installer)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7b02d1f617f7e558acd9c0423dd785c84e0175f195ee0085b2fdc79d66054683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628919"
---
# <a name="session-object-windows-installer"></a>objet Session (Windows Installer)

L’objet **session** contrôle le processus d’installation. Il ouvre la base de données du programme d’installation, qui contient les tables et les données d’installation. Cet objet est associé à un ensemble standard de fonctions d’action, chacune effectuant des opérations particulières sur des données à partir d’une ou plusieurs tables. Des actions personnalisées supplémentaires peuvent être ajoutées pour des installations de produits spécifiques. La fonction de moteur de base est un séquenceur qui extrait les enregistrements séquentiels d’une table de séquences désignée, évalue toute expression de condition spécifiée et exécute l’action désignée. Les actions non reconnues par le moteur sont différées à l’objet gestionnaire d’interface utilisateur pour le traitement, généralement des séquences de boîte de dialogue.

Notez qu’un seul objet de **session** peut être ouvert par un processus unique.

## <a name="members"></a>Membres

L’objet **session** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **session** possède ces méthodes.



| Méthode                                                 | Description                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Action**](session-doaction.md)                   | Exécute l’action spécifiée. <br/>                                                                                                                                                                                                                                |
| [**EvaluateCondition**](session-evaluatecondition.md) | Évalue une expression logique contenant des symboles et des valeurs et retourne un entier de l’énumération msiEvaluateConditionErrorEnum.<br/>                                                                                                                          |
| [**FeatureInfo**](session-featureinfo.md)             | Retourne un objet [**FeatureInfo**](featureinfo-object.md) qui contient des informations descriptives pour la fonctionnalité spécifiée.<br/>                                                                                                                                       |
| [**FormatRecord**](session-formatrecord.md)           | Retourne une chaîne mise en forme à partir de données de modèle et d’enregistrement.<br/>                                                                                                                                                                                                      |
| [**Message**](session-message.md)                     | Exécute toutes les opérations de journalisation activées et diffère l’exécution à l’objet de gestionnaire d’interface utilisateur associé au moteur.<br/>                                                                                                                                              |
| [**Séquence**](session-sequence.md)                   | Ouvre une requête sur la table spécifiée, en ordonnant les actions en fonction des nombres figurant dans la colonne séquence. Pour chaque ligne extraite, la méthode d' [**action**](session-doaction.md) est appelée, à condition que toute expression de condition fournie ne corresponde pas à false.<br/> |
| [**SetInstallLevel**](session-setinstalllevel.md)     | Définit le niveau d’installation de l’installation actuelle sur une valeur spécifiée et recalcule les États SELECT et installed pour toutes les fonctionnalités.<br/>                                                                                                                    |



 

### <a name="properties"></a>Propriétés

L’objet **session** possède ces propriétés.



| Propriété                                                                  | Type d’accès           | Description                                                                                                                                                                |
|:--------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComponentCosts**](session-componentcosts.md)<br/>               |                       | Retourne un objet [**RecordList**](recordlist-object.md) énumérant l’espace disque par lecteur requis pour installer un composant.<br/>                                  |
| [**ComponentCurrentState**](session-componentcurrentstate.md)<br/> |                       | Retourne l’état installé actuel du composant désigné.<br/>                                                                                                |
| [**ComponentRequestState**](session-componentrequeststate.md)<br/> |                       | Obtient ou demande une modification de l’état d’action d’une ligne dans la table des composants.<br/>                                                                               |
| [**Base de données**](session-database.md)<br/>                           |                       | Retourne la base de données pour la session d’installation en cours.<br/>                                                                                                      |
| [**FeatureCost**](session-featurecost.md)<br/>                     |                       | Retourne la quantité totale d’espace disque (en unités de 512 octets) requise par la fonctionnalité spécifiée et ses fonctionnalités parentes (jusqu’à la racine du tableau des fonctionnalités).<br/> |
| [**FeatureCurrentState**](session-featurecurrentstate.md)<br/>     |                       | Retourne l’état installé actuel de la fonctionnalité désignée.<br/>                                                                                                  |
| [**FeatureRequestState**](session-featurerequeststate.md)<br/>     | Lecture/écriture<br/> | Obtient ou demande une modification de l’État SELECT de l’enregistrement et des sous-enregistrements d’une fonctionnalité.<br/>                                                                          |
| [**FeatureValidStates**](session-featurevalidstates.md)<br/>       |                       | Retourne un entier représentant des indicateurs binaires avec chaque bit approprié représentant un état d’installation valide pour la fonctionnalité spécifiée.<br/>                             |
| [**Programme d’installation**](session-installer.md)<br/>                         |                       | Retourne l’objet d’installation actif.<br/>                                                                                                                            |
| [**Language (objet session)**](session-language.md)<br/>          |                       | Représente l’identificateur de langue numérique utilisé par la session d’installation en cours.<br/>                                                                            |
| [**Mode**](session-mode.md)<br/>                                   |                       | Cette propriété est une valeur représentant l’indicateur de mode désigné pour la session d’installation en cours.<br/>                                                            |
| [**ProductProperty**](session-productproperty.md)<br/>             |                       | Représente la valeur de chaîne d’une propriété de programme d’installation nommée.<br/>                                                                                                      |
| [**Propriété (objet session)**](session-session.md)<br/>           | Lecture/écriture<br/> | Récupère les propriétés du produit de la base de données du produit.<br/>                                                                                                         |
| [**SourcePath**](session-sourcepath.md)<br/>                       |                       | Fournit le chemin d’accès complet au dossier désigné sur le média source ou l’image serveur.<br/>                                                                            |
| [**TargetPath**](session-targetpath.md)<br/>                       | Lecture/écriture<br/> | Fournit le chemin d’accès complet au dossier désigné sur le lecteur cible de l’installation.<br/>                                                                               |
| [**VerifyDiskSpace**](session-verifydiskspace.md)<br/>             |                       | Retourne la valeur true si l’espace disque disponible est suffisant, et false si le disque est plein.<br/>                                                                                        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




