---
description: Étant donné que le script d’installation peut être exécuté en dehors de la session d’installation dans laquelle il a été écrit, la session n’existe peut-être plus pendant l’exécution du script d’installation.
ms.assetid: 13174c5d-c810-4b5d-9d1e-60ed30b8c44d
title: Obtention d’informations de contexte pour les actions personnalisées d’exécution différée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cd956509a5b8a4c92e0a53bfa455154a59bcc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218996"
---
# <a name="obtaining-context-information-for-deferred-execution-custom-actions"></a>Obtention d’informations de contexte pour les actions personnalisées d’exécution différée

Étant donné que le script d’installation peut être exécuté en dehors de la session d’installation dans laquelle il a été écrit, la session n’existe peut-être plus pendant l’exécution du script d’installation. Dans ce cas, le handle de session d’origine et les propriétés définies pendant la séquence d’installation ne sont pas disponibles pour une action personnalisée d’exécution différée. Toutes les fonctions qui requièrent un descripteur de session sont limitées à quelques méthodes qui peuvent récupérer des informations de contexte, sinon les propriétés nécessaires pendant l’exécution du script doivent être écrites dans le script d’installation. Par exemple, les actions personnalisées différées qui appellent des bibliothèques de liens dynamiques (dll) passent un handle qui ne peut être utilisé que pour obtenir une quantité très limitée d’informations. Les fonctions qui ne nécessitent pas de descripteur de session sont accessibles à partir d’une action personnalisée différée.

Les actions personnalisées d’exécution différée sont limitées à l’appel des fonctions suivantes qui requièrent un handle.



| Fonction                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)       | Prend en charge un ensemble limité de propriétés lorsqu’il est utilisé avec des [actions personnalisées d’exécution différée](deferred-execution-custom-actions.md): la propriété CustomActionData, la propriété [**ProductCode**](productcode.md) et la propriété [**UserSid**](usersid.md) . Les [actions personnalisées de validation](commit-custom-actions.md) ne peuvent pas utiliser la fonction [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) pour obtenir la propriété [**ProductCode**](productcode.md) . Les actions personnalisées de validation peuvent utiliser la propriété CustomActionData pour obtenir le code du produit.<br/> |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)     | Prend en charge un ensemble limité de propriétés lorsqu’il est utilisé avec des [actions personnalisées d’exécution différée](deferred-execution-custom-actions.md): les propriétés CustomActionData et ProductCode.                                                                                                                                                                                                                                                                                                                                                      |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)               | Lorsqu’elles sont appelées à partir d' [actions personnalisées d’exécution différée](deferred-execution-custom-actions.md), de [validation des actions personnalisées](commit-custom-actions.md)ou de [restaurations personnalisées](rollback-custom-actions.md), [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) retourne true ou false quand il est demandé de vérifier les paramètres de mode MSIRUNMODE \_ , MSIRUNMODE \_ Commit ou MSIRUNMODE \_ Rollback. Les demandes de vérification de tous les autres paramètres de mode d’exécution d’une action personnalisée différée, de validation ou d’annulation renvoient la valeur false.<br/>                       |
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)       | ID de langue numérique du produit actuel. Les [actions personnalisées de validation](commit-custom-actions.md) ne peuvent pas utiliser la fonction [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) . Les actions personnalisées de validation peuvent utiliser la propriété CustomActionData pour récupérer l’ID de langue numérique.<br/>                                                                                                                                                                                                                                                           |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) | Traite les messages d’erreur ou de progression de l’action personnalisée.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

une action personnalisée écrite en JScript ou VBScript requiert l’objet de [**Session**](session-object.md) d’installation. Il s’agit de l' **objet de session** de type et le programme d’installation l’attache au script avec le nom « session ». Étant donné que l’objet **session** n’existe peut-être pas lors d’une restauration de l’installation, une action personnalisée différée écrite dans le script doit utiliser l’une des méthodes ou propriétés suivantes de l’objet **session** pour récupérer son contexte.



| Nom                                                           | Description                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Mode (propriété)**](session-mode.md)                          | Retourne la valeur true pour MSIRUNMODE \_ planifié uniquement.                                                                                       |
| [**Propriété Property (objet session)**](session-session.md)  | Retourne la propriété CustomActionData, la propriété [**ProductCode**](productcode.md) ou la propriété [**UserSid**](usersid.md) .        |
| [**Propriété Language (objet session)**](session-language.md) | Retourne l’ID de langue numérique de la session d’installation.                                                                           |
| [**Message, méthode**](session-message.md)                      | Appelé pour gérer les erreurs et la progression.                                                                                              |
| [**Installer (propriété)**](session-installer.md)                | Retourne l’objet parent, qui est utilisé pour les fonctions qui ne sont pas des sessions, telles que l’accès au registre et la gestion de la configuration du programme d’installation. |



 

Les valeurs de propriété qui sont définies au moment du traitement de la séquence d’installation dans le script peuvent ne pas être disponibles au moment de l’exécution du script. Seul l’ensemble de propriétés limité suivant est toujours accessible aux actions personnalisées pendant l’exécution du script.



| Nom de la propriété                      | Description                                                                                                                                                                                                     |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CustomActionData                   | Valeur au moment où l’action personnalisée est traitée dans la table de séquences. La propriété CustomActionData est uniquement disponible pour les actions personnalisées d’exécution différée. Les actions personnalisées immédiates n’ont pas accès à cette propriété. |
| [**ProductCode**](productcode.md) | Code unique du produit, une chaîne [GUID](guid.md) .                                                                                                                                                         |
| [**UserSID**](usersid.md)         | Défini par le programme d’installation sur l’identificateur de sécurité (SID) de l’utilisateur.                                                                                                                                                   |



 

Si d’autres données de propriété sont requises par l’action personnalisée d’exécution différée, leurs valeurs doivent être stockées dans le script d’installation. Pour ce faire, vous pouvez utiliser une deuxième action personnalisée.

**Pour écrire la valeur d’une propriété dans le script d’installation à utiliser pendant une action personnalisée d’exécution différée**

1.  Insérez une petite action personnalisée dans la séquence d’installation qui définit la propriété d’intérêt pour une propriété portant le même nom que l’action personnalisée d’exécution différée. Par exemple, si la clé primaire de l’action personnalisée d’exécution différée est « MyAction », définissez une propriété nommée « MyAction » sur la propriété X que vous devez récupérer. Vous devez définir la propriété « MyAction » dans la séquence d’installation avant l’action personnalisée « MyAction ». Bien que tout type d’action personnalisée puisse définir les données de contexte, la méthode la plus simple consiste à utiliser une action personnalisée d’assignation de propriété (par exemple, le [type d’action personnalisé 51](custom-action-type-51.md)).
2.  Au moment où la séquence d’installation est traitée, le programme d’installation écrit la valeur de la propriété X dans le script d’exécution comme valeur de la propriété CustomActionData.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des propriétés](about-properties.md)
</dt> <dt>

[Utilisation de propriétés](using-properties.md)
</dt> <dt>

[Référence de propriété](property-reference.md)
</dt> </dl>

 

 




