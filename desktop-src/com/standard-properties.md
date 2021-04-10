---
title: Propriétés standard
description: Propriétés standard
ms.assetid: 08b7c388-a362-4d71-ac24-93675984881f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ab30dd644231c5c11a9f1e4d7ccf9c861ae2fa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031893"
---
# <a name="standard-properties"></a>Propriétés standard

OLE définit un ensemble de DISPID standard pour les trois types de propriétés : contrôle, ambiant et étendu. Les tableaux suivants répertorient ces normes pour les propriétés de contrôle, les propriétés ambiantes et les propriétés étendues.



| Propriété de contrôle                                                                               | Type                             | Description                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BackColor, ForeColor, FillColor, BorderColor<br/>                                        | **\_couleur OLE**<br/>        | Le modèle de couleurs du contrôle<br/>                                                                                                                                                                                                    |
| BackStyle, FillStyle, BorderStyle, BorderWidth, BorderVisible, DrawStyle, DrawWidth<br/> | **short** ou **long**<br/> | Bits qui définissent le comportement visuel d’un contrôle, par exemple s’il est plein ou transparent, avec des bordures épaisses ou fines, des styles de ligne, etc.<br/>                                                                                    |
| Police<br/>                                                                                | **IDispatch \***<br/>      | Police utilisée dans le contrôle, qui est un pointeur **IDispatch** vers un objet de police standard. Pour plus d’informations, consultez [objet de police standard](standard-font-object.md) .<br/>                                                         |
| Légende, texte<br/>                                                                       | **BSTR**<br/>              | Chaînes contenant l’étiquette du contrôle (la légende) ou son contenu textuel (le texte). Notez que la légende ne nomme pas nécessairement le contrôle dans le conteneur. Consultez la propriété nom étendu dans le tableau suivant.<br/> |
| activé<br/>                                                                             | **Boolean**<br/>              | Détermine si le contrôle est activé ou désactivé. Si elle est désactivée, le contrôle est probablement grisé.<br/>                                                                                                                           |
| Fenêtre<br/>                                                                              | **HWND**<br/>              | Handle de fenêtre du contrôle, s’il en a un.<br/>                                                                                                                                                                              |
| Tabulation<br/>                                                                             | **Boolean**<br/>              | Détermine si ce contrôle est un taquet de tabulation.<br/>                                                                                                                                                                                |



 



| Propriété ambiante                         | Type                        | Description                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BackColor, ForeColor<br/>          | **\_couleur OLE**<br/>   | Fournit des contrôles avec les couleurs d’arrière-plan et de premier plan par défaut. L’utilisation de par un contrôle est facultative.<br/>                                                                                                                                                                                                                                                                                          |
| Police<br/>                          | **IDispatch \***<br/> | Pointeur vers un objet de police standard qui définit la police par défaut pour le formulaire. L’utilisation de par un contrôle est facultative. Pour plus d’informations, consultez [objet de police standard](standard-font-object.md) .<br/>                                                                                                                                                                                                    |
| LocaleID<br/>                      | **LCID**<br/>         | Langage utilisé dans le conteneur. L’utilisation par un contrôle est recommandée.<br/>                                                                                                                                                                                                                                                                                                                        |
| UserMode<br/>                      | **Boolean**<br/>         | Décrit si le conteneur est en mode création (**false**) ou en mode exécution (**true**), qu’un contrôle doit utiliser pour modifier ses fonctionnalités disponibles si nécessaire.<br/>                                                                                                                                                                                                                      |
| UIDead<br/>                        | **Boolean**<br/>         | Décrit si le conteneur est dans un mode où les contrôles doivent ignorer l’entrée d’utilisateur. Cela s’applique indépendamment de la méthode de l’application. Un conteneur peut toujours définir UIDead sur **true** en mode Design et peut lui affecter la valeur **true** lorsqu’il a atteint un point d’arrêt ou, par exemple, en mode exécution. Un contrôle doit prêter attention à cette propriété.<br/>                                                                |
| MessageReflect<br/>                | **Boolean**<br/>         | Spécifie si le conteneur souhaite recevoir des messages Windows tels que WM \_ CTLCOLOR, WM \_ DRAWITEM, WM \_ PARENTNOTIFY, et ainsi de suite en tant qu’événements.<br/>                                                                                                                                                                                                                                           |
| SupportsMnemonics<br/>             | **Boolean**<br/>         | Indique si le conteneur traite les mnémoniques ou non. Un contrôle peut faire tout ce qu’il veut avec ces informations, par exemple ne pas souligner les caractères qu’il utiliserait normalement comme mnémoniques.<br/>                                                                                                                                                                                                 |
| ShowGrabHandles, ShowHatching<br/> | **Boolean**<br/>         | Indique si un contrôle doit afficher une bordure hachure ou des poignées de manipulation (dans la bordure hachurée) lorsque l’activité sur place est active. Les contrôles doivent respecter ces propriétés, donnant au conteneur un contrôle optimal sur la personne qui dessine réellement ces bits d’interface utilisateur. Un conteneur de contrôle peut vouloir dessiner son propre au lieu de s’appuyer sur chaque contrôle, auquel cas ces ambiants seront toujours **false**.<br/> |
| DisplayAsDefault<br/>              | **Boolean**<br/>         | Le conteneur expose une **valeur true** pour cette propriété par le biais du site qui contient ce qui est marqué comme bouton par défaut lorsque le contrôle bouton doit se dessiner lui-même avec un frame par défaut plus épais.<br/>                                                                                                                                                                                         |



 



| Propriété étendue          | Type                        | Description                                                           |
|----------------------------|-----------------------------|-----------------------------------------------------------------------|
| Nom<br/>            | **BSTR**<br/>         | Nom du conteneur pour le contrôle.<br/>                      |
| Visible<br/>         | **Boolean**<br/>         | Visibilité du contrôle.<br/>                                  |
| Parent<br/>          | **IDispatch \***<br/> | Dispinterface du formulaire contenant le contrôle.<br/>      |
| Par défaut, annuler<br/> | **Boolean**<br/>         | Indique si ce contrôle est le bouton par défaut ou annuler.<br/> |



 

Toutes ces propriétés standard ont des valeurs DISPID négatives, indiquant leur état standard.

Notez que pour éviter les conflits dans les symboles de programmation pour ces DISPID, toutes les propriétés ambiantes reçoivent des symboles de la propriété ambiante DISPID de la forme \_ \_  comme dans la \_ couleur ambiante DISPID \_ . Tous les autres symboles utilisent la \_ *propriété* DISPID comme d’habitude.

Certaines propriétés ambiantes, ainsi que les propriétés de contrôle, impliquent des couleurs. Le type de **\_ couleur OLE** mentionné dans les tables précédentes peut faire référence à un type **COLORREF** standard, à un index d’une palette, à un index relatif à une palette ou à un index de couleur système utilisé avec la fonction [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) . La fonction [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor) convertit un type de **\_ couleur OLE** en un type **COLORREF** en fonction d’une palette.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle](control-properties.md)
</dt> </dl>

 

