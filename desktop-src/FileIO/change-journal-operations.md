---
description: Codes et structures de contrôle à utiliser avec le journal des modifications du numéro de séquence de mise à jour (USN) du système de fichiers NTFS.
ms.assetid: 2215f0d4-6ac8-42a5-87a5-9c76d1fae3ed
title: Opérations de journal des modifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a52cda51d0efc4cbae1333fc197f42d6a5cc0f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532156"
---
# <a name="change-journal-operations"></a><span data-ttu-id="34c46-103">Opérations de journal des modifications</span><span class="sxs-lookup"><span data-stu-id="34c46-103">Change Journal Operations</span></span>

<span data-ttu-id="34c46-104">La liste suivante identifie les codes de contrôle qui fonctionnent avec le journal des modifications du numéro de séquence de mise à jour (USN) du système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="34c46-104">The following list identifies the control codes that work with the NTFS file system update sequence number (USN) change journal.</span></span>

-   [<span data-ttu-id="34c46-105">**FSCTL \_ créer \_ un \_ journal USN**</span><span class="sxs-lookup"><span data-stu-id="34c46-105">**FSCTL\_CREATE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)
-   [<span data-ttu-id="34c46-106">**FSCTL \_ supprimer \_ le \_ journal USN**</span><span class="sxs-lookup"><span data-stu-id="34c46-106">**FSCTL\_DELETE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal)
-   [<span data-ttu-id="34c46-107">**données USN de l' \_ énumération FSCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="34c46-107">**FSCTL\_ENUM\_USN\_DATA**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)
-   [<span data-ttu-id="34c46-108">**\_descripteur de marque FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="34c46-108">**FSCTL\_MARK\_HANDLE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_mark_handle)
-   [<span data-ttu-id="34c46-109">**\_ \_ journal USN des requêtes FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="34c46-109">**FSCTL\_QUERY\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal)
-   [<span data-ttu-id="34c46-110">**\_ \_ journal USN de lecture FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="34c46-110">**FSCTL\_READ\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal)

<span data-ttu-id="34c46-111">La liste suivante identifie les informations de structures relatives au journal des modifications USN du système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="34c46-111">The following list identifies the structures information that relates to the NTFS file system USN change journal.</span></span>

-   [<span data-ttu-id="34c46-112">**CRÉER \_ des \_ données de journal USN \_**</span><span class="sxs-lookup"><span data-stu-id="34c46-112">**CREATE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data)
-   [<span data-ttu-id="34c46-113">**SUPPRIMER \_ les \_ données du journal USN \_**</span><span class="sxs-lookup"><span data-stu-id="34c46-113">**DELETE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-delete_usn_journal_data)
-   [<span data-ttu-id="34c46-114">**MARQUER \_ les \_ informations du handle**</span><span class="sxs-lookup"><span data-stu-id="34c46-114">**MARK\_HANDLE\_INFO**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mark_handle_info)
-   [<span data-ttu-id="34c46-115">**\_données enum \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="34c46-115">**MFT\_ENUM\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mft_enum_data_v0)
-   [<span data-ttu-id="34c46-116">**LIRE \_ les \_ données du journal USN \_**</span><span class="sxs-lookup"><span data-stu-id="34c46-116">**READ\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0)
-   [<span data-ttu-id="34c46-117">**\_données du journal USN \_**</span><span class="sxs-lookup"><span data-stu-id="34c46-117">**USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0)
-   [<span data-ttu-id="34c46-118">**\_enregistrement USN**</span><span class="sxs-lookup"><span data-stu-id="34c46-118">**USN\_RECORD**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)

 

 
