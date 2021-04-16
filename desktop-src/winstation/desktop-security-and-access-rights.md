---
title: Sécurité des postes de travail et droits d’accès
description: La sécurité vous permet de contrôler l’accès aux objets de bureau. Pour plus d’informations sur la sécurité, consultez Access-Control modèle.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382278"
---
# <a name="desktop-security-and-access-rights"></a>Sécurité des postes de travail et droits d’accès

La sécurité vous permet de contrôler l’accès aux objets de bureau. Pour plus d’informations sur la sécurité, consultez [modèle de contrôle d’accès](/windows/desktop/SecAuthZ/access-control-model).

Vous pouvez spécifier un [descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptors) pour un objet de bureau lorsque vous appelez la fonction [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) ou [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) . Si vous spécifiez NULL, le bureau obtient un descripteur de sécurité par défaut. Les listes de contrôle d’accès dans le descripteur de sécurité par défaut d’un ordinateur de bureau proviennent de sa station de fenêtre parente.

Pour obtenir ou définir le descripteur de sécurité d’un objet de station Windows, appelez les fonctions [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) et [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Lorsque vous appelez la fonction [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) ou [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) , le système vérifie les droits d’accès demandés par rapport au descripteur de sécurité de l’objet.

Les droits d’accès valides pour les objets de bureau incluent les droits d' [accès standard](/windows/desktop/SecAuthZ/standard-access-rights) et certains droits d’accès spécifiques aux objets. Le tableau suivant répertorie les droits d’accès standard utilisés par tous les objets.

| Valeur                       | Signification                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SUPPRIMER (0x00010000L)        | Requis pour supprimer l’objet.                                                                                                                                                                                                                                                       |
| \_Contrôle de lecture (0x00020000L) | Requis pour lire les informations dans le descripteur de sécurité de l’objet, à l’exclusion des informations contenues dans la liste SACL. Pour lire ou écrire dans la liste SACL, vous devez demander le droit d’accès à la \_ sécurité du système Access \_ . Pour plus d’informations, consultez [droit d’accès SACL](/windows/desktop/SecAuthZ/sacl-access-right). |
| SYNCHRONISEr (0x00100000L)   | Non pris en charge pour les objets de bureau.                                                                                                                                                                                                                                                   |
| ÉCRITURE \_ DAC (0x00040000L)    | Requis pour modifier la liste DACL dans le descripteur de sécurité de l’objet.                                                                                                                                                                                                               |
| \_Propriétaire de l’écriture (0x00080000L)  | Requis pour modifier le propriétaire dans le descripteur de sécurité de l’objet.                                                                                                                                                                                                              |



 

Le tableau suivant répertorie les droits d’accès spécifiques aux objets.



| Droit d’accès                       | Description                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| \_CREATEMENU de bureau (0x0004L)      | Requis pour créer un menu sur le bureau.                                                   |
| DESKTOP \_ CREATEWINDOW (0x0002L)    | Requis pour créer une fenêtre sur le bureau.                                                 |
| \_Énumération de postes de travail (0x0040L)       | Requis pour que le Bureau soit énuméré.                                                  |
| \_HOOKCONTROL de bureau (0x0008L)     | Requis pour établir l’un des raccordements de la fenêtre.                                              |
| \_JOURNALPLAYBACK de bureau (0x0020L) | Requis pour effectuer la lecture du journal sur un ordinateur de bureau.                                          |
| \_JOURNALRECORD de bureau (0x0010L)   | Requis pour effectuer l’enregistrement du journal sur un bureau.                                         |
| \_READOBJECTS de bureau (0x0001L)     | Requis pour lire des objets sur le bureau.                                                    |
| \_SWITCHDESKTOP de bureau (0x0100L)   | Requis pour activer le Bureau à l’aide de la fonction [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) . |
| \_WRITEOBJECTS de bureau (0x0080L)    | Requis pour écrire des objets sur le bureau.                                                   |



 

Voici les droits d' [accès génériques](/windows/desktop/SecAuthZ/generic-access-rights) pour un objet de bureau contenu dans la station de fenêtre interactive de la session d’ouverture de session de l’utilisateur.



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
<td><dl> DESKTOP_ENUMERATE<br />
DESKTOP_READOBJECTS<br />
STANDARD_RIGHTS_READ<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_WRITE<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> DESKTOP_SWITCHDESKTOP<br />
STANDARD_RIGHTS_EXECUTE<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_ENUMERATE<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_READOBJECTS<br />
DESKTOP_SWITCHDESKTOP<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_REQUIRED<br />
</dl></td>
</tr>
</tbody>
</table>



 

Vous pouvez demander le \_ \_ droit d’accès à la sécurité du système d’accès à un objet de bureau si vous souhaitez lire ou écrire la liste SACL de l’objet. Pour plus d’informations, consultez [listes de contrôle d’accès (ACL)](/windows/desktop/SecAuthZ/access-control-lists) et [droit d’accès SACL](/windows/desktop/SecAuthZ/sacl-access-right).

 

 