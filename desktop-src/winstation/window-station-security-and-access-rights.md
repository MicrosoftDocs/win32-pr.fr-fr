---
title: Sécurité de station Windows et droits d’accès
description: La sécurité vous permet de contrôler l’accès aux objets de station Windows. Pour plus d’informations sur la sécurité, consultez Access-Control modèle.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522141"
---
# <a name="window-station-security-and-access-rights"></a>Sécurité de station Windows et droits d’accès

La sécurité vous permet de contrôler l’accès aux objets de station Windows. Pour plus d’informations sur la sécurité, consultez [modèle de contrôle d’accès](/windows/desktop/SecAuthZ/access-control-model).

Vous pouvez spécifier un [descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptors) pour un objet de station Windows lorsque vous appelez la fonction [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) . Si vous spécifiez la valeur NULL, la station Windows obtient un descripteur de sécurité par défaut. Les listes de contrôle d’accès dans le descripteur de sécurité par défaut d’une station Windows proviennent du jeton principal ou d’emprunt d’identité du créateur.

Pour obtenir ou définir le descripteur de sécurité d’un objet de station Windows, appelez les fonctions [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) et [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Lorsque vous appelez la fonction [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) , le système vérifie les droits d’accès demandés par rapport au descripteur de sécurité de l’objet.

Les droits d’accès valides pour les objets de station Windows incluent les [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights) et certains droits d’accès spécifiques aux objets. Le tableau suivant répertorie les droits d’accès standard utilisés par tous les objets.

| Valeur                       | Signification                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SUPPRIMER (0x00010000L)        | Requis pour supprimer l’objet.                                                                                                                                                                                                                                                       |
| \_Contrôle de lecture (0x00020000L) | Requis pour lire les informations dans le descripteur de sécurité de l’objet, à l’exclusion des informations contenues dans la liste SACL. Pour lire ou écrire dans la liste SACL, vous devez demander le droit d’accès à la \_ sécurité du système Access \_ . Pour plus d’informations, consultez [droit d’accès SACL](/windows/desktop/SecAuthZ/sacl-access-right). |
| SYNCHRONISEr (0x00100000L)   | Non pris en charge pour les objets de station Windows.                                                                                                                                                                                                                                            |
| ÉCRITURE \_ DAC (0x00040000L)    | Requis pour modifier la liste DACL dans le descripteur de sécurité de l’objet.                                                                                                                                                                                                               |
| \_Propriétaire de l’écriture (0x00080000L)  | Requis pour modifier le propriétaire dans le descripteur de sécurité de l’objet.                                                                                                                                                                                                              |



 

Le tableau suivant répertorie les droits d’accès spécifiques aux objets.



| Droit d’accès                        | Description                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WINSTA \_ tous les \_ accès (0x37F)         | Tous les droits d’accès possibles pour la station Windows.                                                                                                                                                                                                                            |
| WINSTA \_ ACCESSCLIPBOARD (0x0004L)   | Requis pour utiliser le presse-papiers.                                                                                                                                                                                                                                                |
| WINSTA \_ ACCESSGLOBALATOMS (0x0020L) | Requis pour manipuler les atomes globaux.                                                                                                                                                                                                                                          |
| WINSTA \_ CREATEDESKTOP (0x0008L)     | Requis pour créer de nouveaux objets de bureau sur la station Windows.                                                                                                                                                                                                                 |
| WINSTA \_ ENUMDESKTOPS (0x0001L)      | Requis pour énumérer les objets de bureau existants.                                                                                                                                                                                                                               |
| \_Énumération WINSTA (0x0100L)         | Requis pour que la station de fenêtre soit énumérée.                                                                                                                                                                                                                             |
| WINSTA \_ EXITWINDOWS (0x0040L)       | Requis pour appeler correctement la fonction [**exitwindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) ou [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) . Les stations de Windows peuvent être partagées par les utilisateurs et ce type d’accès peut empêcher les autres utilisateurs d’une station Windows de se déconnecter du propriétaire de la station Windows. |
| WINSTA \_ READATTRIBUTES (0x0002L)    | Requis pour lire les attributs d’un objet de station Windows. Cet attribut comprend des paramètres de couleur et d’autres propriétés de station de fenêtre globale.                                                                                                                                |
| WINSTA \_ READSCREEN (0x0200L)        | Requis pour accéder au contenu de l’écran.                                                                                                                                                                                                                                           |
| WINSTA \_ WRITEATTRIBUTES (0x0010L)   | Requis pour modifier les attributs d’un objet de station Windows. Les attributs incluent les paramètres de couleur et d’autres propriétés de la station de fenêtre globale.                                                                                                                               |



 

Vous trouverez ci-dessous les [droits d’accès génériques](/windows/desktop/SecAuthZ/generic-access-rights) pour l’objet de station Windows Interactive, qui est la station Windows affectée à la session d’ouverture de session de l’utilisateur interactif.



<table>
<thead>
<tr class="header">
<th>Droit d’accès</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GENERIC_READ</td>
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

Vous trouverez ci-dessous les [droits d’accès génériques](/windows/desktop/SecAuthZ/generic-access-rights) pour un objet de station Windows non interactive. Le système affecte les stations Windows non interactives à toutes les sessions d’ouverture de session autres que celles de l’utilisateur interactif.



<table>
<thead>
<tr class="header">
<th>Droit d’accès</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GENERIC_READ</td>
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

Vous pouvez demander le \_ droit accès à la sécurité du système d’accès \_ à un objet de station Windows si vous souhaitez lire ou écrire la liste SACL de l’objet. Pour plus d’informations, consultez [listes de contrôle d’accès (ACL)](/windows/desktop/SecAuthZ/access-control-lists) et [droit d’accès SACL](/windows/desktop/SecAuthZ/sacl-access-right).

 

 